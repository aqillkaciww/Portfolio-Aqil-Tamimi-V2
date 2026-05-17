<template>
  <section class="cred-section" id="credentials">
    <div class="cred-inner">

      <div class="cred-col">
        <div class="cred-header">
          <span class="cred-icon">🏅</span>
          <h2 class="cred-title">Certifications</h2>
        </div>
        <div class="cred-list">
          <div v-for="cert in certifications" :key="cert.name" class="cred-item">
            <div class="cred-item-main">
              <span class="cred-name">{{ cert.name }}</span>
              <span class="cred-year">{{ cert.year }}</span>
            </div>
            <span class="cred-issuer">{{ cert.issuer }}</span>
          </div>
        </div>
      </div>

      <!-- Divider -->
      <div class="cred-divider"></div>

      <!-- Education -->
      <div class="cred-col">
        <div class="cred-header">
          <span class="cred-icon">🎓</span>
          <h2 class="cred-title">Education</h2>
        </div>
        <div class="cred-list">
          <div v-for="edu in education" :key="edu.name" class="cred-item">
            <div class="cred-item-main">
              <span class="cred-name">{{ edu.name }}</span>
              <span class="cred-year">{{ edu.year }}</span>
            </div>
            <span class="cred-issuer">{{ edu.institution }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Certification {
  name: string
  issuer: string
  year: string
  link: string
}

interface Education {
  name: string
  institution: string
  year: string
}

const certifications: Certification[] = [
  {
    name: 'MikroTik Certified Network Associate (MTCNA)',
    issuer: 'MikroTik',
    year: '2025',
  },
  {
    name: 'Technoversary - EcoDigital for Environment',
    issuer: 'HIMATI UNIKU',
    year: '2025',
  }
]

const education: Education[] = [
  {
    name: 'Sistem Informasi Jaringan dan Aplikasi',
    institution: 'SMK Negeri 2 Yogyakarta',
    year: '2023–Now'
  }
]
</script>
