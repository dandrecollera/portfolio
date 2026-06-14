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

    <section class="relative w-full bg-neutral-950 text-white z-20 border-t border-neutral-900/50">
      <div class="max-w-4xl mx-auto py-28 px-8">
        <div ref="projectsHeader" class="mb-16 invisible">
          <h2 class="font-sans font-bold text-5xl mb-4 tracking-tight">Projects</h2>
          <p class="font-sans font-light text-lg text-neutral-400">
            Production pipelines, backend systems, and automated data architectures.
          </p>
        </div>

        <div ref="projectsList" class="space-y-12">
          <div 
            v-for="(project, index) in projectsData" 
            :key="project.title"
            class="group border border-neutral-900 bg-neutral-950/40 hover:bg-neutral-950 hover:border-neutral-800 transition-all duration-300 rounded-2xl p-8 invisible project-row"
          >
            <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-2 mb-4">
              <div class="flex items-center gap-3">
                <span class="text-xs font-mono text-neutral-600">0{{ index + 1 }}</span>
                <h3 class="font-sans font-bold text-2xl text-neutral-100 group-hover:text-white transition-colors">
                  {{ project.title }}
                </h3>
              </div>
              
              <a 
                v-if="project.url" 
                :href="project.url" 
                target="_blank" 
                rel="noopener noreferrer"
                class="inline-flex items-center gap-1.5 text-xs font-sans font-light tracking-wider uppercase text-neutral-400 hover:text-white transition-colors duration-200"
              >
                Launch App
                <svg class="w-3 h-3 transform group-hover:translate-x-0.5 group-hover:-translate-y-0.5 transition-transform" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2.5" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                </svg>
              </a>
              <span v-else class="text-xs font-mono tracking-wider text-neutral-600 uppercase">
                Internal System
              </span>
            </div>

            <p class="font-sans font-light text-sm text-neutral-400 leading-relaxed mb-6">
              {{ project.description }}
            </p>

            <div class="flex flex-wrap gap-2">
              <span 
                v-for="tech in project.tags" 
                :key="tech"
                class="text-xs font-mono bg-neutral-900 border border-neutral-800/60 text-neutral-400 rounded-md py-1 px-2.5"
              >
                {{ tech }}
              </span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <footer class="relative w-full h-[40vh] bg-black overflow-hidden border-t border-neutral-900/60 z-20">
      <TopoFooterCanvas />
      
      <div class="absolute inset-0 flex flex-col justify-between p-8 md:p-12 pointer-events-none z-30">
        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4 w-full max-w-5xl mx-auto pointer-events-auto">
          <div>
            <p class="font-sans font-medium text-sm text-neutral-300">Dandre Mitchel Collera</p>
            <p class="font-sans font-light text-xs text-neutral-500 mt-1">Fullstack Engineer & Backend Expert</p>
          </div>
          <div class="flex items-center gap-6 text-xs font-mono tracking-wider text-neutral-400 uppercase">
            <a href="https://github.com/dandrecollera" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">GitHub</a>
            <a href="https://www.linkedin.com/in/dandrecollera/" target="_blank" rel="noopener noreferrer" class="hover:text-white transition-colors">LinkedIn</a>
          </div>
        </div>

        <div class="w-full max-w-5xl mx-auto flex justify-between items-center border-t border-neutral-900/80 pt-6">
          <p class="text-[10px] font-mono text-neutral-600 uppercase tracking-widest">
            © 2026 All Rights Reserved
          </p>
          <p class="text-[10px] font-mono text-neutral-600 uppercase tracking-widest">
            Precision & Execution
          </p>
        </div>
      </div>
    </footer>

  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
import TopoCanvas from './components/TopoCanvas.vue'
import TopoFooterCanvas from './components/TopoFooterCanvas.vue'
import { gsap } from 'gsap'
import { ScrollTrigger } from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

const heroText = ref(null)
const aboutHeader = ref(null)
const philosophyCard = ref(null)
const strategyCards = ref(null)
const deepDiveRows = ref(null)
const skillsHeader = ref(null)
const projectsHeader = ref(null)
const projectsList = ref(null)

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

  gsap.fromTo(projectsHeader.value,
    { autoAlpha: 0, y: 30 },
    {
      autoAlpha: 1, y: 0, duration: 1, ease: 'power3.out',
      scrollTrigger: { trigger: projectsHeader.value, start: 'top 85%' }
    }
  )

  gsap.fromTo('.project-row',
    { autoAlpha: 0, y: 40 },
    {
      autoAlpha: 1, y: 0, duration: 1, ease: 'power3.out', stagger: 0.2,
      scrollTrigger: { trigger: projectsList.value, start: 'top 80%' }
    }
  )
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
    { name: 'Vite', iconClass: 'devicon-vitejs-plain' },
    { name: 'Tailwind CSS', iconClass: 'devicon-tailwindcss-original' },
    { name: 'DaisyUI', iconClass: 'devicon-css3-plain' },
    { name: 'Bootstrap', iconClass: 'devicon-bootstrap-plain' }
  ]
}

const projectsData = [
  {
    title: 'TIFTCI Backend Service',
    description: 'Engineered a dedicated backend optimization service using Laravel to overhaul the platform’s data layers. Streamlined core database management systems, refactored raw query logic to eliminate processing bottlenecks, and implemented secure architectural practices to deliver a high-speed, secure, and low-latency infrastructure.',
    url: 'https://tiftci.com/',
    tags: ['Laravel', 'PHP', 'MySQL', 'Database Optimization', 'Security']
  },
  {
    title: 'Inrico Philippines Website',
    description: 'Developed a high-performance product catalog platform for Inrico two-way radio hardware within the local market. Engineered a custom WordPress plugin from scratch to securely handle client inquiries and intake forms, while implementing aggressive optimization mechanics and targeted local SEO strategies to anchor the site at the top of Google search rankings.',
    url: 'https://inricoph.com/',
    tags: ['WordPress', 'Custom Plugin', 'MySQL', 'SEO', 'Performance Optimization']
  },
  {
    title: 'OrbitalSEO Website Tracker',
    description: 'Architected a centralized monitoring platform using Next.js to track and audit large fleets of client WordPress installations. Built an automated headless runtime pipeline with Puppeteer to capture visual snapshots, instantly tracking visual regressions, downtime events, and precise page modification timestamps for real-time system observability.',
    url: '',
    tags: ['Next.js', 'Puppeteer', 'Chromium', 'Automation', 'Web Scraping']
  },
  {
    title: 'OrbitalSEO Data Scraping API',
    description: 'Built a resilient, headless web scraping pipeline using Puppeteer and Chromium to continuously extract and compile high-volume marketplace data into a structured client database. Integrated a secure API layer and automation triggers to seamlessly pipe the cached datasets into separate cross-project dependencies.',
    url: '',
    tags: ['Puppeteer', 'Chromium', 'Node.js', 'API Automation']
  },
  {
    title: 'Domain Name Verifier & Audit',
    description: 'Engineered a network utility platform using Python and Flask to analyze domain state and availability. Integrated optimized Perl scripts to handle underlying system sockets, allowing users to query, fetch, and audit unstructured raw WHOIS registry datasets with minimal execution latency.',
    url: '',
    tags: ['Python', 'Flask', 'Perl', 'WHOIS API', 'Network Security']
  },
  {
    title: 'Access Healthcare Staffing Job Board',
    description: 'Developed a dynamic job board platform built on Laravel 8 that integrates with the LaborEdge API to aggregate, sync, and display live healthcare employment opportunities. Architected transactional email dispatch pipelines using Zoho Mail to instantly route job details and match candidate profiles directly to recruiting staff.',
    url: '',
    tags: ['Laravel 8', 'PHP', 'LaborEdge API', 'Zoho Mail', 'Automation']
  },
  {
    title: 'Access Healthcare Staffing Central API & ATS',
    description: 'Engineered a mission-critical Central API and Applicant Tracking System (ATS) to manage high-volume staffing operations. Built multi-directional automation syncs across RingCentral, Ambition, and Job Robotix platforms, while executing extensive backend refactoring and database optimizations to significantly reduce server resource consumption.',
    url: '',
    tags: ['Laravel 12', 'PHP', 'Redis', 'API Automation', 'Performance Optimization']
  },
  {
    title: 'Access Healthcare Staffing AI API',
    description: 'Engineered a localized AI processing microservice leveraging LangChain, Ollama, and DeepSeek models. Developed specialized intelligent data pipelines to automate resume parsing, execution of automated document verification, and real-time validation of workforce timesheets with high semantic accuracy.',
    url: '',
    tags: ['Python', 'LangChain', 'Ollama', 'DeepSeek', 'AI Automation']
  }
]
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