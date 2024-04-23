<template>
  <section class="my-skills">
    <div class="container">
      <h2 class="title">My Skills</h2>

      <p class="paragraph">With more than 6 years of experience in software development.</p>

      <div class="skill-list">
        <skill-list v-for="(skill, index) in skills" :key="`my-skill-${index}`" v-bind="skill" />
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

import SkillList from './SkillList.vue';

const skills = ref([
  {
    skillName: 'Frontend',
    skillDetails: [
      'HTML5',
      'CCS3 (Flex - Grid)',
      'Javascript',
      'Vue',
      'React'
    ],
  },
  {
    skillName: 'Backend',
    skillDetails: [
      'PHP (Laravel)',
      'Java (Spring Boot)',
      'Node (Express, Nest, Typescript)'
    ],
  },
  {
    skillName: 'Database',
    skillDetails: [
      'MySQL',
      'SQL Server',
      'PostgreSQL',
      'MongoDB'
    ],
  },
  {
    skillName: 'Architecture',
    skillDetails: [
      'MVC',
      'Hexagonal',
      'Clean Code',
      'SOLID',
      'YAGNI',
      'DRY'
    ],
  },
  {
    skillName: 'Additional',
    skillDetails: [
      'Docker',
      'Git',
      'VPS (DigitalOcean, DreamHost)',
      'Linux'
    ],
  },
]);
</script>

<style scoped>
@import '../css/my-skills-component.css';
</style>
