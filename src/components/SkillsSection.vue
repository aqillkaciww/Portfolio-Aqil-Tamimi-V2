<template>
  <section class="skills-section" id="skills">
    <div class="skills-inner">
      <div class="section-header">
        <h2 class="section-title center">Tech Stack</h2>
        <p class="section-subtitle">
          Teknologi yang saya gunakan dalam pengembangan website yang interaktif juga responsif.
        </p>
      </div>

      <div class="skills-grid">
        <div v-for="skill in skills" :key="skill.name" class="skill-card">
          <div class="skill-icon" :style="{ backgroundColor: skill.bgColor }">
            <img :src="skill.icon" :alt="skill.name" width="40" height="40" />
          </div>
          <h3 class="skill-name">{{ skill.name }}</h3>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Skill {
  name: string
  icon: string
  bgColor: string
}

const skills: Skill[] = [
  {
    name: 'Next.js',
    icon: '/nextjs.png',
    bgColor: 'transparent',
  },
  {
    name: 'Tailwind',
    icon: '/tailwind-css.png',
    bgColor: 'transparent',
  },
  {
    name: 'TypeScript',
    icon: '/typescript.png',
    bgColor: 'transparent',
  },
  {
    name: 'HTML',
    icon: '/html5.png',
    bgColor: 'transparent',
  },
  {
    name: 'CSS',
    icon: '/css3.png',
    bgColor: 'transparent',
  },
]
</script>
