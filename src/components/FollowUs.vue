<template>
  <h2 class="title">Follow us</h2>

  <span class="follow-message"><message-contact /></span>

  <div class="container-social">
    <div class="social-media-icon" v-for="social in socialNetworks" :key="social.link">
      <div class="icon">
        <img :src="social.icon" :alt="social.alt">
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';

import MessageContact from "./MessageContact.vue";

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
