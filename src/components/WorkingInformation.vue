<template>
  <div class="timeline">
    <div class="h-separator"></div>

    <p class="time-worked">{{ timeWorked }}</p>

    <div class="working-information">
      <h5 class="job-company">{{ jobCompany }}</h5>

      <p class="job-description">
        <span class="preview" v-if="readMore">{{ description }}</span>
        <span class="description" v-if="!readMore">{{ jobDescription }}</span>
      </p>
      <p class="read-more" @click="toggle">{{ readMoreTitle }}</p>

      <p class="job-address">{{ jobAddress }}</p>
    </div>
  </div>
</template>

<script setup>
import { defineProps, ref, computed } from 'vue';

const props = defineProps({
  timeWorked: String,
  jobCompany: String,
  jobDescription: String,
  jobAddress: String,
});

const readMoreTitle = ref('Read more');

const maxLength = 150;

const readMore = ref(() => props.jobDescription.length > maxLength);

const description = computed(() => readMore.value ? props.jobDescription.slice(0, maxLength).trim() + '...' : props.jobDescription);

function toggle () {
  readMore.value = !readMore.value;
  readMoreTitle.value = readMore.value ? 'Read more' : 'Close';
}
</script>
