<template>
  <section class="skills-section" id="skills">
    <div class="skills-inner">
      <div class="section-header">
        <h2 class="section-title center">The Toolset</h2>
        <p class="section-subtitle">
          My craft is built with intentional tools, carefully chosen frameworks, and a love for well-structured elegance that breathes life into the experience.
        </p>
      </div>

      <div class="skills-grid">
        <div v-for="skill in skills" :key="skill.name" class="skill-card">
          <div class="skill-icon" :style="{ backgroundColor: skill.bgColor }">
            <span class="skill-icon-text">{{ skill.icon }}</span>
          </div>
          <div class="skill-body">
            <h3 class="skill-name">{{ skill.name }}</h3>
            <p class="skill-desc">{{ skill.desc }}</p>
            <div class="skill-tags">
              <span v-for="tag in skill.tags" :key="tag" class="skill-tag">{{ tag }}</span>
            </div>
          </div>
        </div>

        <!-- Highlight Card -->
        <div class="skill-card skill-card-highlight">
          <div class="skill-highlight-icon">⚡</div>
          <h3 class="skill-name">Quick Learner</h3>
          <p class="skill-desc">
            Passionate about the craft and always finding new tools. From bleeding-edge frameworks to classic design fundamentals.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const skills = [
  {
    name: 'React & Next.js',
    icon: '⚛',
    bgColor: 'rgba(97,218,251,0.12)',
    desc: 'Building modern, high-performance applications that bring joy to both developers and end users.',
    tags: ['Components', 'App Router', 'SSR']
  },
  {
    name: 'Vue.js',
    icon: '◈',
    bgColor: 'rgba(66,184,131,0.12)',
    desc: 'Crafting reactive interfaces with clean and thoughtful compositions for seamless user experiences.',
    tags: ['Vue 3', 'Composition API', 'Vite']
  },
  {
    name: 'Tailwind CSS',
    icon: '🎨',
    bgColor: 'rgba(56,189,248,0.12)',
    desc: 'Translating visual concepts into pixel-perfect, accessible, and responsive designs with precision.',
    tags: ['Responsive', 'Animations', 'Dark Mode']
  },
  {
    name: 'TypeScript',
    icon: 'TS',
    bgColor: 'rgba(49,120,198,0.12)',
    desc: 'Writing strong, maintainable code that scales with confidence through robust type safety.',
    tags: ['Type Safety', 'Generics', 'Interfaces']
  },
  {
    name: 'UI/UX Design',
    icon: '✦',
    bgColor: 'rgba(167,139,250,0.12)',
    desc: 'Bridging the gap between aesthetics and functionality — designing experiences that feel intuitive.',
    tags: ['Figma', 'Wireframing', 'Prototyping']
  }
]
</script>
