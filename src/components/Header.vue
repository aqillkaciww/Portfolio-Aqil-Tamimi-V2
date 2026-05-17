<template>
  <header class="header">
    <div class="header-container">
      <!-- Logo/Brand -->
      <div class="logo">
        <span class="brand-name">{{ brandName }}</span>
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
  brandName?: string;
  navItems?: string[];
  ctaText?: string;
}

const props = withDefaults(defineProps<Props>(), {
  brandName: 'Starlit Studio',
  navItems: () => ['Work', 'Process', 'About', 'Contact'],
  ctaText: 'Hire Me'
});

const handleHireClick = () => {
  console.log('Hire Me button clicked');
  // Nanti bisa ditambah navigasi ke contact section
};
</script>


