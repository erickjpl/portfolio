<template>
  <div class="skill">
    <div class="container-circle">
      <h3 class="percentage">{{ percentage }}%</h3>
    </div>

    <h5 class="skill-name">{{ skillName }}</h5>
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

defineProps({
  percentage: String,
  skillName: String,
});
</script>
