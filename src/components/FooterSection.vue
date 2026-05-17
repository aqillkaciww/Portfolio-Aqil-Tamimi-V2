<template>
  <footer class="footer" id="footer">
    <div class="footer-inner">
      <!-- Top Row -->
      <div class="footer-top">
        <div class="footer-brand">
          <span class="footer-logo">Muhammad Aqil Tamimi</span>
          <p class="footer-tagline">
            Crafting serene digital experiences with a painter's touch and a developer's precision.
          </p>
        </div>

        <nav class="footer-nav">
          <div class="footer-nav-col" v-for="col in navCols" :key="col.title">
            <h4 class="footer-nav-title">{{ col.title }}</h4>

            <ul class="footer-nav-list">
              <li v-for="item in col.items" :key="item.name">
                <a
                  :href="item.link"
                  class="footer-nav-link"
                  :target="item.link.startsWith('http') ? '_blank' : '_self'"
                >
                  {{ item.name }}
                </a>
              </li>
            </ul>
          </div>
        </nav>
      </div>

      <!-- Divider -->
      <div class="footer-divider"></div>

      <!-- Bottom Row -->
      <div class="footer-bottom">
        <p class="footer-copy">
          © {{ currentYear }} Muhammad Aqil Tamimi. Crafted with care and curiosity.
        </p>

        <div class="footer-socials">
          <!-- GitHub -->
          <a
            href="https://github.com/aqillkaciww"
            target="_blank"
            class="footer-social-link"
            aria-label="GitHub"
          >
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0 0 24 12c0-6.63-5.37-12-12-12z"
              />
            </svg>
          </a>

          <!-- Instagram -->
          <a
            href="https://instagram.com/akilltaa"
            target="_blank"
            class="footer-social-link"
            aria-label="Instagram"
          >
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M7.75 2C4.574 2 2 4.574 2 7.75v8.5C2 19.426 4.574 22 7.75 22h8.5C19.426 22 22 19.426 22 16.25v-8.5C22 4.574 19.426 2 16.25 2h-8.5zm0 1.5h8.5A4.25 4.25 0 0 1 20.5 7.75v8.5a4.25 4.25 0 0 1-4.25 4.25h-8.5A4.25 4.25 0 0 1 3.5 16.25v-8.5A4.25 4.25 0 0 1 7.75 3.5zm8.75 1a1 1 0 1 0 0 2 1 1 0 0 0 0-2zM12 7a5 5 0 1 0 0 10 5 5 0 0 0 0-10zm0 1.5A3.5 3.5 0 1 1 8.5 12 3.5 3.5 0 0 1 12 8.5z"
              />
            </svg>
          </a>

          <!-- Email -->
          <a href="mailto:aqiltamimi6@gmail.com" class="footer-social-link" aria-label="Email">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="currentColor">
              <path
                d="M2 5.5A2.5 2.5 0 0 1 4.5 3h15A2.5 2.5 0 0 1 22 5.5v13a2.5 2.5 0 0 1-2.5 2.5h-15A2.5 2.5 0 0 1 2 18.5v-13zm2.2-.5 7.8 6.24L19.8 5H4.2zm15.8 2.16-7.37 5.9a1 1 0 0 1-1.26 0L4 7.16V18.5c0 .55.45 1 1 1h14c.55 0 1-.45 1-1V7.16z"
              />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
interface NavItem {
  name: string
  link: string
}

interface NavCol {
  title: string
  items: NavItem[]
}

const currentYear = new Date().getFullYear()

const navCols: NavCol[] = [
  {
    title: 'Navigate',
    items: [
      { name: 'Home', link: '#' },
      { name: 'About', link: '#about' },
      { name: 'Tech', link: '#skills' },
      { name: 'Projects', link: '#projects' },
    ],
  },
  {
    title: 'Connect',
    items: [
      { name: 'Contact', link: '#contact' },
      { name: 'GitHub', link: 'https://github.com/aqillkaciww' },
      { name: 'Instagram', link: 'https://instagram.com/akilltaa' },
    ],
  },
]
</script>
