<template>
  <div class="skills">
    <h5 class="skill-name">{{ skillName }}</h5>
    <ol class="skill-details">
      <li v-for="(detail, index) in skillDetails" :key="`skills-${index}`">{{ detail }}</li>
    </ol>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  skillName: String,
  skillDetails: Array
});
</script>
