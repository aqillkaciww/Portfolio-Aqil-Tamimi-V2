<template>
  <section class="contact-section" id="contact">
    <div class="contact-inner">
      <!-- Left: CTA -->
      <div class="contact-copy">
        <h2 class="contact-title">Let's sow the seeds of a<br />new project.</h2>
        <p class="contact-desc">
          Whether you have a grand vision or a humble sketch — I am fully devoted to cultivating it into something beautiful. Tell me about your dreams and let's make something grow.
        </p>
        <div class="contact-info-list">
          <a href="mailto:aqil@example.com" class="contact-info-item">
            <div class="contact-info-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"></path>
                <polyline points="22,6 12,13 2,6"></polyline>
              </svg>
            </div>
            <span>aqiltamimi@example.com</span>
          </a>
          <div class="contact-info-item">
            <div class="contact-info-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path>
                <circle cx="12" cy="10" r="3"></circle>
              </svg>
            </div>
            <span>Bandar Lampung, Indonesia</span>
          </div>
          <div class="contact-info-item">
            <div class="contact-info-icon">
              <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
                <rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect>
                <line x1="16" y1="2" x2="16" y2="6"></line>
                <line x1="8" y1="2" x2="8" y2="6"></line>
                <line x1="3" y1="10" x2="21" y2="10"></line>
              </svg>
            </div>
            <span>Mon – Sat &nbsp;|&nbsp; 08.00 – 18.00 WIB</span>
          </div>
        </div>
      </div>

      <!-- Right: Form -->
      <div class="contact-form-card">
        <form @submit.prevent="handleSubmit" class="contact-form">
          <div class="form-row">
            <div class="form-group">
              <label for="contact-name">Full Name</label>
              <input id="contact-name" v-model="form.name" type="text" placeholder="Your full name" required />
            </div>
            <div class="form-group">
              <label for="contact-email">Your Email</label>
              <input id="contact-email" v-model="form.email" type="email" placeholder="your@email.com" required />
            </div>
          </div>
          <div class="form-group">
            <label for="contact-message">Your Message</label>
            <textarea id="contact-message" v-model="form.message" rows="5" placeholder="Tell me about your project..." required></textarea>
          </div>
          <button type="submit" class="contact-submit">
            Send Message
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <line x1="22" y1="2" x2="11" y2="13"></line>
              <polygon points="22 2 15 22 11 13 2 9 22 2"></polygon>
            </svg>
          </button>
        </form>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  message: ''
})

const handleSubmit = () => {
  console.log('Form submitted:', form)
  // Handle submission
}
</script>
