<template>
  <section class="hero-section">
    <div class="hero-inner">
      <div class="hero-copy">
        <span class="hero-label">{{ props.pretitle }}</span>
        <h1 class="hero-title">
          {{ props.titleLeading }} <span class="hero-title-accent">{{ props.titleAccent }}</span>
          {{ props.titleTrailing }}
        </h1>
        <p class="hero-description">{{ props.description }}</p>

        <div class="hero-actions">
          <button class="hero-button hero-button-primary">{{ props.primaryAction }}</button>
          <button class="hero-button hero-button-secondary">{{ props.secondaryAction }}</button>
        </div>
      </div>

      <div class="hero-card">
        <div class="art-card">
          <div class="art-sky"></div>
          <div class="art-cloud art-cloud-1"></div>
          <div class="art-cloud art-cloud-2"></div>
          <div class="art-hills"></div>
          <div class="art-forest"></div>
          <div class="art-house"></div>
        </div>
        <div class="hero-quote">"Code is poetry in motion."</div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
interface Props {
  pretitle?: string;
  titleLeading?: string;
  titleAccent?: string;
  titleTrailing?: string;
  description?: string;
  primaryAction?: string;
  secondaryAction?: string;
}

const props = withDefaults(defineProps<Props>(), {
  pretitle: 'Available for craft-driven projects',
  titleLeading: "Crafting digital spaces with a",
  titleAccent: "painter's touch",
  titleTrailing: "and a developer's precision.",
  description:
    'I am a Frontend Developer specializing in building serene, highly-functional web experiences that feel as warm as a hand-drawn illustration.',
  primaryAction: 'Skills',
  secondaryAction: 'Projects'
});
</script>
