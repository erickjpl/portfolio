<template>
  <section class="about-me">
    <div class="container">
      <h2 class="title">About me</h2>

      <p class="paragraph">My career in software development has been marked by a
        journey of continuous growth and evolution, where my commitment to quality standards and ethics
        has been fundamental. Each experience has served as a stepping stone towards personal and
        professional excellence. From the outset, I have embraced challenges with enthusiasm,
        contributing to the development of various projects.</p>

      <p class="paragraph">Over time, I have consistently demonstrated my ability to
        adapt to diverse project requirements, refining my skills and expanding my knowledge base. My
        dedication to continuous learning and development has been a constant throughout my career. My
        achievements include not only technical successes such as process automation and high
        availability implementations but also significant personal growth.</p>

      <div class="wrapper-skills">
        <skill-component v-for="(skill, index) in skills" :key="`skill-${index}`" v-bind="skill" />
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue';

import SkillComponent from './SkillComponent.vue';

const skills = ref([
  {
    percentage: '72',
    skillName: 'Frontend',
  },
  {
    percentage: '91',
    skillName: 'Backend',
  },
  {
    percentage: '87',
    skillName: 'Database',
  },
  {
    percentage: '84',
    skillName: 'Architecture',
  }
]);
</script>

<style scoped>
@import '../css/about-component.css';
</style>
