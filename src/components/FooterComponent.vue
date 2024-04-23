<template>
  <footer class="footer">
    <div class="container">
      <div class="content">
        <div class="logo">
          <a href="#"><img src="../assets/logo-nombre-ligth.png" alt="Logo Erick"></a>
        </div>

        <div class="links">
          <p class="subtitle">Links</p>

          <ul>
            <li><a href="#about">Acerca de</a></li>
            <li><a href="#portfolio">Portafolio</a></li>
            <li><a href="#contact">Contacto</a></li>
          </ul>
        </div>

        <div class="social">
          <p class="subtitle">Follow us</p>

          <div class="social-media-icon" v-for="social in socialNetworks" :key="social.link">
            <div class="icon">
              <img :src="social.icon" :alt="social.alt">
            </div>
          </div>
        </div>
      </div>

      <div class="info">
        <p>&copy; {{ year }} <span class="info-name">Erick Pérez</span></p>
        <p>All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const date = new Date()
const year = date.getFullYear()


import { ref } from 'vue';

const socialNetworks = ref([
  {
    icon: require('../assets/220343-e29886f9.png'),
    link: '#1',
    alt: 'Icon LinkedIn',
  },
  {
    icon: require('../assets/1051377-346b657b.png'),
    link: '#2',
    alt: 'Icon GitHub',
  },
  {
    icon: require('../assets/5968958-356aaac6.png'),
    link: '#3',
    alt: 'Icon Twitter',
  }
]);
</script>

<style scoped>
@import '../css/footer-component.css';
</style>
