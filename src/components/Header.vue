<template>
  <header class="header">
    <div class="header-container">
      <!-- Logo/Brand -->
      <div class="logo">
        <span class="head-name">{{ headName }}</span>
      </div>

      <!-- Navigation Menu -->
      <nav class="nav-menu">
        <ul class="nav-list">
          <li v-for="item in navItems" :key="item" class="nav-item">
            <a href="#" class="nav-link">{{ item }}</a>
          </li>
        </ul>
      </nav>

      <!-- CTA Button -->
      <button class="cta-button" @click="handleHireClick">
        {{ ctaText }}
      </button>
    </div>
  </header>
</template>

<script setup lang="ts">
interface Props {
  headName?: string;
  navItems?: string[];
  ctaText?: string;
}

const props = withDefaults(defineProps<Props>(), {
  headName: 'Aqil Tamimi',
  navItems: () => ['Work', 'Process', 'About', 'Contact'],
  ctaText: 'Hire Me'
});

const handleHireClick = () => {
  console.log('Hire button clicked');
};
</script>


