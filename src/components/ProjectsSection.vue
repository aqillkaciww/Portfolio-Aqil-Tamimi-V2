<template>
  <section class="pro-section" id="projects">
    <div class="projects-inner">
      <div class="section-header">
        <h2 class="section-title center">Projects</h2>
        <p class="section-subtitle">
          Di bawah ini adalah beberapa proyek yang telah saya kerjakan.
        </p>
      </div>

      <div class="timeline">
        <div v-for="item in projects" :key="item.id" class="timeline-item">
          <div class="timeline-dot">
            <div class="timeline-dot-inner"></div>
          </div>
          <div class="timeline-card">
            <div class="timeline-card-inner">
              <div v-if="item.image" class="project-image">
                <img :src="item.image" :alt="item.company + ' logo'" />
              </div>
              <div class="timeline-card-body">
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
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Project {
  id: number
  role: string
  company: string
  image?: string
  start: string
  end: string
  desc: string
  tags: string[]
}

const projects: Project[] = [
  {
    id: 1,
    role: 'Echoopedia - Education Platform',
    company: 'Technoversary',
    image: '/echoopedia.png',
    start: 'Nov 2025',
    end: 'Des 2025',
    desc: 'Platform edukasi dan aksi lingkungan yang mendukung kampanye hijau, pengelolaan sampah, serta upaya menciptakan masa depan yang lebih berkelanjutan.',
    tags: ['Next.js', 'TypeScript'],
  },
  {
    id: 2,
    role: 'Coklaxe - Pemesanan Villa Online',
    company: 'Startup Agency',
    image: '/coklaxe.png',
    start: 'Sep 2023',
    end: 'Okt 2023',
    desc: "Website pemesanan villa online. Ini adalah proyek website pertama saya saat masih duduk di bangku kelas 10 SMK yang saya kembangkan menggunakan HTML dan CSS.",
    tags: ['HTML5', 'CSS3',],
  },
]
</script>
