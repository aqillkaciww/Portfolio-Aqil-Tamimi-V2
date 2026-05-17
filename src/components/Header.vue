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

<style scoped>
.header {
  background-color: #f5f1ed;
  padding: 20px 40px;
  position: sticky;
  top: 0;
  z-index: 100;
}

.header-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  flex-shrink: 0;
}

.brand-name {
  font-size: 20px;
  font-weight: 600;
  color: #2a2a2a;
  letter-spacing: 0.5px;
}

.nav-menu {
  flex: 1;
  display: flex;
  justify-content: center;
  margin: 0 40px;
}

.nav-list {
  list-style: none;
  display: flex;
  gap: 40px;
  margin: 0;
  padding: 0;
}

.nav-item {
  margin: 0;
}

.nav-link {
  text-decoration: none;
  color: #2a2a2a;
  font-size: 14px;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-link:hover {
  color: #7b9b5f;
}

.cta-button {
  background-color: #2a2a2a;
  color: #f5f1ed;
  border: none;
  padding: 10px 24px;
  border-radius: 4px;
  font-size: 14px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease;
  flex-shrink: 0;
}

.cta-button:hover {
  background-color: #444;
}

@media (max-width: 768px) {
  .header-container {
    flex-wrap: wrap;
    gap: 20px;
  }

  .nav-menu {
    margin: 0;
    width: 100%;
    order: 3;
  }

  .nav-list {
    gap: 20px;
  }
}
</style>
