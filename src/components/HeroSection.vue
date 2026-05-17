<template>
  <section class="hero-section">
    <div class="hero-inner">
      <div class="hero-copy">
        <span class="hero-label">{{ props.pretitle }}</span>
        <h1 class="hero-title">
          {{ props.titleLeading }} <br />
          <span>{{ props.titleTrailing }}</span>
        </h1>
        <p class="hero-description">{{ props.description }}</p>

        <div class="hero-actions">
          <a class="hero-button hero-button-primary" href="#skills">{{ props.primaryAction }}</a>
          <a class="hero-button hero-button-secondary" href="#projects">{{props.secondaryAction}}</a>
        </div>
      </div>

      <div class="hero-card">
        <img src="/hero-image-1.jpg" alt="Aqil Tamimi" class="hero-photo" />
        <!-- <div class="art-card">
            <div class="art-sky"></div>
            <div class="art-cloud art-cloud-1"></div>
            <div class="art-cloud art-cloud-2"></div>
            <div class="art-hills"></div>
            <div class="art-forest"></div>
            <div class="art-house"></div>
          </div> -->
        <div class="hero-quote">"Setiap detail memiliki arti, setiap interaksi memiliki tujuan."</div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Props {
  pretitle?: string
  titleLeading?: string
  titleTrailing?: string
  description?: string
  primaryAction?: string
  secondaryAction?: string
}

const props = withDefaults(defineProps<Props>(), {
  pretitle: '</> Hello World!',
  titleLeading: 'Every detail has meaning,',
  titleTrailing: 'every interaction has a purpose.',
  description:
    'Saya adalah seorang Frontend Developer yang berfokus pada pengembangan web yang interaktif, fungsional, dan nyaman digunakan.',
  primaryAction: 'Skills',
  secondaryAction: 'Projects',
})
</script>
