<template>
  <div ref="containerRef" class="topo-section">
    <canvas ref="canvasRef" id="topo-canvas"></canvas>
    <div class="glass-overlay"></div>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from 'vue'
import * as THREE from 'three'
import vertexShader from '../shaders/topo.vert'
import fragmentShader from '../shaders/topo.frag'

const canvasRef = ref(null)
const containerRef = ref(null)

let renderer, scene, camera, geometry, material, bgMesh, clock, animationFrameId
let isVisible = true
let observer

const uniforms = {
  u_time: { value: 0.0 },
  u_resolution: { value: new THREE.Vector2(window.innerWidth, window.innerHeight) },
  u_mouse: { value: new THREE.Vector2(0.5, 0.5) },
}

const handleMouseMove = (e) => {
  if (!isVisible) return
  uniforms.u_mouse.value.x = e.clientX / window.innerWidth
  uniforms.u_mouse.value.y = 1.0 - e.clientY / window.innerHeight
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

  uniforms.u_time.value = clock.getElapsedTime()
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

  animate()

  observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => { isVisible = entry.isIntersecting })
  }, { threshold: 0.05 })
  if (containerRef.value) observer.observe(containerRef.value)

  window.addEventListener('mousemove', handleMouseMove, { passive: true })
  window.addEventListener('resize', handleResize)
})

onBeforeUnmount(() => {
  window.removeEventListener('mousemove', handleMouseMove)
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
#topo-canvas, .glass-overlay {
  position: absolute; 
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
#topo-canvas { z-index: 1; }
.glass-overlay {
  z-index: 2;
  backdrop-filter: blur(0.7px);
  pointer-events: none;
}
</style>