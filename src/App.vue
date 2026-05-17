<script setup lang="ts">
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import CredentialsSection from './components/CredentialsSection.vue'
import FooterSection from './components/FooterSection.vue'
</script>

<template>
  <Header />
  <main>
    <HeroSection />
    <AboutSection />
    <SkillsSection />
    <ProjectsSection />
    <CredentialsSection />
  </main>
  <FooterSection />
</template>
