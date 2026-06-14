<template>
  <div ref="containerRef" class="topo-section">
    <canvas ref="canvasRef" id="topo-footer-canvas"></canvas>
    <div class="glass-overlay"></div>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import * as THREE from 'three'
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js'
import vertexShader from '../shaders/topo.vert'
import fragmentShader from '../shaders/topo.frag'

const canvasRef = ref(null)
const containerRef = ref(null)

const flowerConfig = {
  position: { x: 1, y: -2.3, z: 3 },
  scale: 4.2,
  swaySpeed: 0.5,       
  swayIntensity: 0.04,  
}

let renderer, scene, camera, geometry, material, bgMesh, clock, animationFrameId
let flowerModel = null
let isVisible = true
let observer

const uniforms = {
  u_time: { value: 0.0 },
  u_resolution: { value: new THREE.Vector2(window.innerWidth, window.innerHeight) },
  u_mouse: { value: new THREE.Vector2(0.5, 0.5) }, 
}

const handleResize = () => {
  if (!renderer) return
  const width = window.innerWidth
  const height = window.innerHeight

  camera.aspect = width / height
  camera.updateProjectionMatrix()

  renderer.setSize(width, height)
  renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))
  uniforms.u_resolution.value.set(width, height)
}

const animate = () => {
  animationFrameId = requestAnimationFrame(animate)
  if (!isVisible) return

  const elapsedTime = clock.getElapsedTime()
  uniforms.u_time.value = elapsedTime

  if (flowerModel) {
    const t = elapsedTime * flowerConfig.swaySpeed
    flowerModel.rotation.z = Math.sin(t) * flowerConfig.swayIntensity
    flowerModel.rotation.x = 0.2 + Math.cos(t * 0.75) * (flowerConfig.swayIntensity * 0.6)
    flowerModel.position.y = flowerConfig.position.y + (Math.sin(t * 0.6) * 0.05)
  }

  renderer.render(scene, camera)
}

onMounted(() => {
  scene = new THREE.Scene()
  camera = new THREE.PerspectiveCamera(45, window.innerWidth / window.innerHeight, 0.1, 100)
  camera.position.z = 5
  clock = new THREE.Clock()

  renderer = new THREE.WebGLRenderer({
    canvas: canvasRef.value,
    antialias: true,
    alpha: true,
    powerPreference: "high-performance"
  })
  renderer.setSize(window.innerWidth, window.innerHeight)
  renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2))

  geometry = new THREE.PlaneGeometry(10, 10)
  material = new THREE.ShaderMaterial({
    vertexShader,
    fragmentShader,
    uniforms,
    depthWrite: false 
  })
  bgMesh = new THREE.Mesh(geometry, material)
  bgMesh.position.z = -2
  scene.add(bgMesh)

  const ambientLight = new THREE.AmbientLight(0xffffff, 0.5)
  scene.add(ambientLight)

  const keyLight = new THREE.DirectionalLight(0xffffff, 1.8) 
  keyLight.position.set(5, 3, 3)
  scene.add(keyLight)

  const fillLight = new THREE.DirectionalLight(0xffffff, 1.0)
  fillLight.position.set(-5, 2, 2)
  scene.add(fillLight)

  const loader = new GLTFLoader()
  loader.load(
    '/models/flower.glb',
    (gltf) => {
      flowerModel = gltf.scene
      flowerModel.position.set(flowerConfig.position.x, flowerConfig.position.y, flowerConfig.position.z)
      flowerModel.scale.set(flowerConfig.scale, flowerConfig.scale, flowerConfig.scale) 
      flowerModel.rotation.set(0.2, Math.PI * -0.2, 0)

      flowerModel.traverse((child) => {
        if (child.isMesh && child.material) {
          child.material = child.material.clone()
          child.material.onBeforeCompile = (shader) => {
            shader.fragmentShader = shader.fragmentShader.replace(
              '#include <dithering_fragment>',
              `
              #include <dithering_fragment>
              float grayscale = dot(gl_FragColor.rgb, vec3(0.299, 0.587, 0.114));
              gl_FragColor.rgb = vec3(grayscale);
              `
            )
          }
        }
      })
      scene.add(flowerModel)
    },
    undefined,
    (error) => { console.error('Error loading flower:', error) }
  )

  animate()

  observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => { isVisible = entry.isIntersecting })
  }, { threshold: 0.05 })
  if (containerRef.value) observer.observe(containerRef.value)

  window.addEventListener('resize', handleResize)
})

onBeforeUnmount(() => {
  window.removeEventListener('resize', handleResize)
  cancelAnimationFrame(animationFrameId)
  if (observer) observer.disconnect()
  if (geometry) geometry.dispose()
  if (material) material.dispose()
  if (renderer) renderer.dispose()
})
</script>

<style scoped>
.topo-section {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}
#topo-footer-canvas, .glass-overlay {
  position: absolute; 
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
#topo-footer-canvas { z-index: 1; }
.glass-overlay {
  z-index: 2;
  backdrop-filter: blur(0.7px);
  pointer-events: none;
}
</style>