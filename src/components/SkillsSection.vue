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
            <span class="skill-icon-text">{{ skill.icon }}</span>
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
    icon: 'Next',
    bgColor: 'rgba(54,65,89,0.08)',
  },
  {
    name: 'Tailwind',
    icon: 'TW',
    bgColor: 'rgba(56,189,248,0.14)',
  },
  {
    name: 'Laravel',
    icon: 'Lv',
    bgColor: 'rgba(245,101,101,0.14)',
  },
  {
    name: 'TypeScript',
    icon: 'TS',
    bgColor: 'rgba(49,120,198,0.14)',
  },
  {
    name: 'HTML',
    icon: '</>',
    bgColor: 'rgba(251,146,60,0.14)',
  },
  {
    name: 'CSS',
    icon: 'CSS',
    bgColor: 'rgba(56,189,248,0.14)',
  },
]
</script>
