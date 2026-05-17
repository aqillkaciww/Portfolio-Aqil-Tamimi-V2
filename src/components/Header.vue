<template>
  <header class="header">
    <div class="header-container">
      <!-- Logo/Brand -->
      <div class="logo">
        <a :href="headHref" class="logo-link" aria-label="Home">
          <span class="head-name">{{ headName }}</span>
        </a>
      </div>

      <!-- Navigation Menu -->
      <nav class="nav-menu">
        <ul class="nav-list">
          <li v-for="item in navItems" :key="item" class="nav-item">
            <a href="#" class="nav-link">{{ item }}</a>
          </li>
        </ul>
      </nav>

      <!-- CTA Button replaced by download-button -->
      <button class="download-button" @click="handleDownloadClick">
        <div class="docs">
          <svg
            viewBox="0 0 24 24"
            width="20"
            height="20"
            stroke="currentColor"
            stroke-width="2"
            fill="none"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="icon-docs"
          >
            <path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"></path>
            <polyline points="14 2 14 8 20 8"></polyline>
            <line x1="16" y1="13" x2="8" y2="13"></line>
            <line x1="16" y1="17" x2="8" y2="17"></line>
            <polyline points="10 9 9 9 8 9"></polyline>
          </svg>
          Download CV
        </div>
      </button>
    </div>
  </header>
</template>

<script setup lang="ts">
interface Props {
  headName?: string;
  navItems?: string[];
  ctaText?: string;
  headHref?: string;
}

const props = withDefaults(defineProps<Props>(), {
  headName: 'Aqil Tamimi',
  navItems: () => ['Work', 'Process', 'About', 'Contact'],
  ctaText: 'Download CV',
  headHref: '/'
});

const handleDownloadClick = () => {
  console.log('Download CV button clicked');
};
</script>


