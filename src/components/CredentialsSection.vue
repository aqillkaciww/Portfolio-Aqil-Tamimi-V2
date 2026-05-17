<template>
  <section class="cred-section" id="credentials">
    <div class="cred-inner">
      <!-- Certifications -->
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
const certifications = [
  {
    name: 'React Advanced License',
    issuer: 'Meta / Coursera',
    year: '2024'
  },
  {
    name: 'Google UI Design',
    issuer: 'Google / Coursera',
    year: '2023'
  },
  {
    name: 'Belajar Front-end (Dicoding)',
    issuer: 'Dicoding Indonesia',
    year: '2022'
  }
]

const education = [
  {
    name: 'S1 Ilmu Komputer',
    institution: 'Universitas of Lampung',
    year: '2022–Now'
  },
  {
    name: 'SMK Jurusan IT',
    institution: 'SMK Teknologi',
    year: '2019–2022'
  }
]
</script>
