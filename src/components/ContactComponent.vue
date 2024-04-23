<template>
  <section class="contact-me">
    <div class="container">
      <div class="side-follow-us">
        <follow-us />
      </div>

      <div class="side-contact-me">
        <contact-me />
      </div>
    </div>
  </section>
</template>

<script setup>
import FollowUs from './FollowUs.vue';
import ContactMe from './ContactMe.vue';
</script>

<style scoped>
@import '../css/contact-component.css';
</style>
