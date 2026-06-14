<template>
  <div class="w-full bg-black text-white">

    <section class="relative w-full h-screen overflow-hidden">
      <TopoCanvas />

      <div class="absolute inset-y-0 left-8 md:left-24 flex flex-col justify-center leading-none -space-y-4 md:-space-y-8 opacity-45 pointer-events-none z-10 select-none">
        <h1 class="font-gothic text-7xl md:text-9xl text-outline font-normal tracking-wide">
          Dandre Collera
        </h1>
      </div>

      <div class="absolute inset-0 flex flex-col justify-center items-start px-8 md:px-24 bg-black/10 pointer-events-none">
        <div ref="heroText" class="relative z-30 pointer-events-auto mt-4 invisible">
          <p class="font-sans font-light tracking-widest text-sm uppercase text-gray-200 mb-0">
            Fullstack Engineer & Backend Expert
          </p>
          
          <h2 class="font-sans font-bold text-5xl md:text-8xl tracking-tight text-white transition-colors duration-300 cursor-default drop-shadow-[0_4px_12px_rgba(0,0,0,0.8)]">
            Dandre Mitchel Collera
          </h2>

          <p class="mb-5 mt-3 md:my-0 text-gray-300 font-light">Backend architecture, interactive web design & system optimization.</p>
          <p class="text-gray-300 font-light">Where technical precision meets fluid execution.</p>
        </div>
      </div>
    </section>

    <section class="relative w-full bg-neutral-950 text-white z-20 border-t border-neutral-900/50">
      <div class="max-w-4xl mx-auto py-28 px-8">
        <div ref="aboutHeader" class="mb-16 invisible">
          <h2 class="font-sans font-bold text-5xl mb-4 tracking-tight">About Me</h2>
          <p class="font-sans font-light text-lg text-neutral-400">
            Philosophy, execution, and core development principles.
          </p>
        </div>
        
        <div ref="philosophyCard" class="bg-black border border-neutral-900 rounded-2xl p-8 md:p-10 mb-16 shadow-xl transition-all duration-300 hover:border-neutral-800 invisible">
          <h3 class="text-xs uppercase tracking-[0.25em] text-neutral-500 font-bold mb-4">The Philosophy</h3>
          <p class="font-sans font-light text-xl md:text-2xl text-neutral-200 leading-relaxed">
            "I believe that complexity is a liability. The best solutions are simple, transparent, and inherently effective."
          </p>
          <p class="font-sans font-light text-base text-neutral-400 mt-4 leading-relaxed border-t border-neutral-900/80 pt-4">
            Whether I am architecting a backend database or styling a user interface, my goal is always the same: to build clean, highly optimized systems that are easy to maintain today and effortless for the next developer to understand tomorrow.
          </p>
        </div>

        <div ref="strategyCards" class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-16">
          <div class="bg-black border border-neutral-900 rounded-2xl p-8 transition-all duration-300 hover:border-neutral-800 invisible strategy-card">
            <h3 class="text-xs uppercase tracking-[0.25em] text-neutral-500 font-bold mb-4">What I Do</h3>
            <p class="font-sans font-light text-sm text-neutral-400 leading-relaxed">
              I am a backend-focused engineer with a deep appreciation for minimalist visual design. While my daily routines are heavily technical, my background in hobbyist graphic design influences how I structure code—treating logic maps, schemas, and layouts with the same structural balance and precision.
            </p>
          </div>

          <div class="bg-black border border-neutral-900 rounded-2xl p-8 transition-all duration-300 hover:border-neutral-800 flex flex-col justify-between invisible strategy-card">
            <div>
              <h3 class="text-xs uppercase tracking-[0.25em] text-neutral-500 font-bold mb-4">The Execution</h3>
              <p class="font-sans font-light text-sm text-neutral-400 leading-relaxed">
                I don't over-engineer. I write code for performance, scalability, and longevity, delivering digital products where engineering precision meets structural clarity.
              </p>
            </div>
          </div>
        </div>

        <div ref="deepDiveRows" class="space-y-6">
          <div class="group border border-neutral-900 bg-black hover:border-neutral-800 transition-all duration-300 rounded-xl p-6 flex flex-col md:flex-row md:items-start gap-4 invisible dive-row">
            <div class="md:w-1/4">
              <span class="text-xs font-mono uppercase tracking-wider text-neutral-500 block mt-1">01 / CORE</span>
              <h4 class="font-sans font-semibold text-base text-white mt-0.5">Backend & Optimization</h4>
            </div>
            <div class="md:w-3/4">
              <p class="font-sans font-light text-sm text-neutral-400 leading-relaxed group-hover:text-neutral-300 transition-colors">
                I specialize in building heavy infrastructure, asynchronous APIs, and writing highly optimized queries. I thrive on solving complex, messy backend challenges—like executing massive multi-gigabyte data migrations and designing lightweight data parsing pipelines using <span class="text-white">Laravel (PHP)</span> and <span class="text-white">FastAPI (Python)</span>.
              </p>
            </div>
          </div>

          <div class="group border border-neutral-900 bg-black hover:border-neutral-800 transition-all duration-300 rounded-xl p-6 flex flex-col md:flex-row md:items-start gap-4 invisible dive-row">
            <div class="md:w-1/4">
              <span class="text-xs font-mono uppercase tracking-wider text-neutral-500 block mt-1">02 / INTERACTION</span>
              <h4 class="font-sans font-semibold text-base text-white mt-0.5">Frontend & Design</h4>
            </div>
            <div class="md:w-3/4">
              <p class="font-sans font-light text-sm text-neutral-400 leading-relaxed group-hover:text-neutral-300 transition-colors">
                I don't just hand off data to the frontend; I bridge the gap. I build responsive, clean interfaces using <span class="text-white">Vue.js, Tailwind CSS, and Bootstrap</span> to support development teams and ensure the visual execution matches the engine's speed under the hood.
              </p>
            </div>
          </div>
        </div>

      </div>
    </section>

    <section class="relative w-full bg-black text-white z-20 border-t border-neutral-900">
      <link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css" />

      <div class="max-w-4xl mx-auto py-24 px-8">
        <div ref="skillsHeader" class="mb-14 invisible">
          <h2 class="font-sans font-bold text-5xl mb-4">Expertise & Stack</h2>
          <p class="font-sans font-light text-lg text-neutral-400">
            Systems, languages, and pipeline mechanics I work with daily.
          </p>
        </div>

        <div class="space-y-12">
          <div v-for="(group, groupName) in skillsData" :key="groupName" class="skill-category">
            <h3 class="text-xs uppercase tracking-[0.25em] text-neutral-500 font-bold mb-5 block border-b border-neutral-900 pb-2">
              {{ groupName }}
            </h3>
            
            <div class="flex flex-wrap gap-3 pill-container">
              <div 
                v-for="skill in group" 
                :key="skill.name" 
                class="flex items-center gap-3 bg-neutral-950 border border-neutral-900 hover:border-neutral-700 transition-all duration-300 rounded-full py-2.5 px-5 group cursor-default select-none shadow-md invisible skill-pill"
              >
                <div class="w-5 h-5 flex items-center justify-center text-xl text-neutral-500 group-hover:text-white transition-colors duration-300">
                  <i :class="skill.iconClass"></i>
                </div>
                <span class="font-sans text-sm font-light text-neutral-300 group-hover:text-white transition-colors duration-300">
                  {{ skill.name }}
                </span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import TopoCanvas from './components/TopoCanvas.vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const heroText = ref(null)
const aboutHeader = ref(null)
const philosophyCard = ref(null)
const strategyCards = ref(null)
const deepDiveRows = ref(null)
const skillsHeader = ref(null)

onMounted(() => {
  gsap.fromTo(heroText.value, 
    { autoAlpha: 0, y: 40 },
    { autoAlpha: 1, y: 0, duration: 1.2, ease: 'power4.out', delay: 0.2 }
  )

  gsap.fromTo(aboutHeader.value,
    { autoAlpha: 0, x: -30 },
    {
      autoAlpha: 1, x: 0, duration: 1, ease: 'power3.out',
      scrollTrigger: { trigger: aboutHeader.value, start: 'top 85%' }
    }
  )
  gsap.fromTo('.header-line', { width: 0 }, { width: 48, duration: 1.2, ease: 'power3.inOut', scrollTrigger: { trigger: aboutHeader.value, start: 'top 85%' } })

  gsap.fromTo(philosophyCard.value,
    { autoAlpha: 0, y: 50 },
    {
      autoAlpha: 1, y: 0, duration: 1.2, ease: 'power3.out',
      scrollTrigger: { trigger: philosophyCard.value, start: 'top 80%' }
    }
  )

  gsap.fromTo('.strategy-card',
    { autoAlpha: 0, y: 40 },
    {
      autoAlpha: 1, y: 0, duration: 1, ease: 'power3.out', stagger: 0.2,
      scrollTrigger: { trigger: strategyCards.value, start: 'top 80%' }
    }
  )

  gsap.fromTo('.dive-row',
    { autoAlpha: 0, y: 30 },
    {
      autoAlpha: 1, y: 0, duration: 1, ease: 'power2.out', stagger: 0.15,
      scrollTrigger: { trigger: deepDiveRows.value, start: 'top 85%' }
    }
  )

  gsap.fromTo(skillsHeader.value,
    { autoAlpha: 0, y: 30 },
    {
      autoAlpha: 1, y: 0, duration: 1, ease: 'power3.out',
      scrollTrigger: { trigger: skillsHeader.value, start: 'top 85%' }
    }
  )

  document.querySelectorAll('.pill-container').forEach((container) => {
    const pills = container.querySelectorAll('.skill-pill')
    gsap.fromTo(pills,
      { autoAlpha: 0, scale: 0.9, y: 15 },
      {
        autoAlpha: 1, scale: 1, y: 0, duration: 0.6, ease: 'back.out(1.2)', stagger: 0.05,
        scrollTrigger: {
          trigger: container,
          start: 'top 90%',
          toggleActions: 'play none none none'
        }
      }
    )
  })
})

const skillsData = {
  'Languages': [
    { name: 'PHP', iconClass: 'devicon-php-plain' },
    { name: 'Python', iconClass: 'devicon-python-plain' },
    { name: 'SQL', iconClass: 'devicon-azuresqldatabase-plain' },
    { name: 'JavaScript / TypeScript', iconClass: 'devicon-typescript-plain' }
  ],
  'Frameworks, CMS & Ecosystems': [
    { name: 'Laravel', iconClass: 'devicon-laravel-original' },
    { name: 'Symfony', iconClass: 'devicon-symfony-original' },
    { name: 'CodeIgniter', iconClass: 'devicon-codeigniter-plain' },
    { name: 'CakePHP', iconClass: 'devicon-cakephp-plain' },
    { name: 'Next.js', iconClass: 'devicon-nextjs-plain' },
    { name: 'WordPress', iconClass: 'devicon-wordpress-plain' },
    { name: 'FastAPI', iconClass: 'devicon-fastapi-plain' },
    { name: 'Vue.js (Composition API)', iconClass: 'devicon-vuejs-plain' }
  ],
  'AI Engineering & Workflows': [
    { name: 'Cursor', iconClass: 'devicon-vscode-plain' },
    { name: 'Claude Code', iconClass: 'devicon-bash-plain' },
    { name: 'Ollama', iconClass: 'devicon-linux-plain' },
    { name: 'Large Language Models (LLMs)', iconClass: 'devicon-openapi-plain' },
    { name: 'v0 by Vercel', iconClass: 'devicon-vercel-line' },
    { name: 'LangChain', iconClass: 'devicon-python-plain' }
  ],
  'Data Scraping & Automation': [
    { name: 'Puppeteer', iconClass: 'devicon-puppeteer-plain' },
    { name: 'Chromium', iconClass: 'devicon-chrome-plain' },
    { name: 'Data Scraping & Pipelines', iconClass: 'devicon-javascript-plain' },
    { name: 'AI Creation & Prompt Engineering', iconClass: 'devicon-openapi-plain' }
  ],
  'Databases, Caching & Infrastructure': [
    { name: 'MySQL', iconClass: 'devicon-mysql-original' },
    { name: 'PostgreSQL', iconClass: 'devicon-postgresql-plain' },
    { name: 'SQL Server', iconClass: 'devicon-microsoftsqlserver-plain' },
    { name: 'Redis', iconClass: 'devicon-redis-plain' },
    { name: 'Cloudflare', iconClass: 'devicon-cloudflare-plain' },
    { name: 'DO Spaces / AWS S3', iconClass: 'devicon-amazonwebservices-plain-wordmark' }
  ],
  'DevOps & Deployment Automation': [
    { name: 'Docker', iconClass: 'devicon-docker-plain' },
    { name: 'GitHub Actions', iconClass: 'devicon-githubactions-plain' },
    { name: 'GitHub', iconClass: 'devicon-github-original' },
    { name: 'Linux / PM2', iconClass: 'devicon-linux-plain' }
  ],
  'UI, Styling & Layout': [
    { name: 'Tailwind CSS', iconClass: 'devicon-tailwindcss-original' },
    { name: 'DaisyUI', iconClass: 'devicon-css3-plain' },
    { name: 'Bootstrap', iconClass: 'devicon-bootstrap-plain' }
  ]
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=UnifrakturMaguntia&display=swap');

.font-gothic {
  font-family: 'UnifrakturMaguntia', Georgia, serif;
}

.font-sans {
  font-family: "Bahnschrift", "Segoe UI", system-ui, sans-serif;
}

.text-outline {
  color: transparent;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: rgba(255, 255, 255, 0.5);
}
</style>