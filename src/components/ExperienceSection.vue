<template>
  <section class="experience-section" id="experience">
    <div class="experience-inner">
      <div class="section-header">
        <h2 class="section-title center">The Journey So Far</h2>
        <p class="section-subtitle">
          Positions I've held, problems I've solved, and lessons I've learned along the way.
        </p>
      </div>

      <div class="timeline">
        <div
          v-for="(item, index) in experiences"
          :key="item.id"
          class="timeline-item"
          :class="{ 'timeline-item-right': index % 2 !== 0 }"
        >
          <div class="timeline-dot">
            <div class="timeline-dot-inner"></div>
          </div>
          <div class="timeline-card">
            <div class="timeline-card-header">
              <div>
                <h3 class="timeline-role">{{ item.role }}</h3>
                <p class="timeline-company">{{ item.company }}</p>
              </div>
              <div class="timeline-period">
                <span class="timeline-date">{{ item.start }}</span>
                <span class="timeline-sep">—</span>
                <span class="timeline-date">{{ item.end }}</span>
              </div>
            </div>
            <p class="timeline-desc">{{ item.desc }}</p>
            <div class="timeline-tags">
              <span v-for="tag in item.tags" :key="tag" class="timeline-tag">{{ tag }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
const experiences = [
  {
    id: 1,
    role: 'Senior Frontend Developer',
    company: 'Freelance & Remote',
    start: 'Jan 2024',
    end: 'Present',
    desc: 'Delivering high-quality digital products for various clients across industries. From concept to launch, creating beautiful and functional web experiences.',
    tags: ['Vue.js', 'React', 'TypeScript', 'Figma']
  },
  {
    id: 2,
    role: 'UI Developer',
    company: 'Startup Agency',
    start: '2022',
    end: '2024',
    desc: 'Crafting front-end for creative agencies. Building UI components and responsive layouts that tell their clients\' stories with precision and flair.',
    tags: ['React', 'GSAP', 'Tailwind CSS']
  },
  {
    id: 3,
    role: 'Junior Web Crafter',
    company: 'Early Stage Agency',
    start: '2020',
    end: '2022',
    desc: 'First hands-on experience with HTML, CSS and JavaScript, learning the most beautiful things that the web has to offer through passionate mentors.',
    tags: ['HTML', 'CSS', 'JavaScript']
  }
]
</script>
