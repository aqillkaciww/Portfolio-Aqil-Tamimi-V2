<template>
  <header class="header">
    <div class="header-container">
      <!-- Logo/Brand -->
      <div class="logo">
        <a :href="props.headHref" class="logo-link" aria-label="Home">
          <span class="head-name">{{ props.headName }}</span>
        </a>
      </div>

      <!-- Navigation Menu -->
      <nav class="nav-menu">
        <ul class="nav-list">
          <li v-for="item in navLinks" :key="item.label" class="nav-item">
            <a :href="item.href" class="nav-link">{{ item.label }}</a>
          </li>
        </ul>
      </nav>

      <!-- CTA Button -->
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
          {{ props.ctaText }}
        </div>
      </button>
    </div>
  </header>
</template>

<script setup lang="ts">
defineOptions({ name: 'AppHeader' })

interface NavLink {
  label: string;
  href: string;
}

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
  headHref: '#',
});


const navLinks: NavLink[] = [
  { label: 'Home', href: '#' },
  { label: 'About', href: '#about' },
  { label: 'Tech', href: '#skills' },
  { label: 'Projects', href: '#projects' }
];

const handleDownloadClick = () => {
  const link = document.createElement('a');
  link.href = '/Aqil-Tamimi-CV.pdf';         // path relatif dari folder public/
  link.download = 'Aqil-Tamimi-CV.pdf';  // nama file saat didownload
  link.click();
};

</script>


