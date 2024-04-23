<template>
  <section class="experiences">
    <h2 class="title">Experiences</h2>

    <p class="paragraph">
      A journey marked by passion, dedication, and teamwork,
      which have served as the fundamental pillars for overcoming challenging goals with determination and focus.
    </p>

    <working-information v-for="(experience, index) in experiences" :key="index" v-bind="experience" />

    <a href="#" class="btn-primary">
      Contact me
      <span class="u-file-icon u-icon u-text-white u-icon-1"><img src="images/959159-5d3ea7b7.png" alt=""></span>
    </a>
  </section>
</template>

<script setup>
import { ref } from 'vue';
import WorkingInformation from './WorkingInformation.vue';

const experiences = ref([
  {
    timeWorked: 'May, 2020 – Dic, 2023',
    jobCompany: 'Application Developer - VALLEVERDE',
    jobDescription: `In my role, I
      significantly contributed to the company's digital transformation by developing and maintaining
      critical sales applications. This included the creation of a new Android application for wholesale
      sales, the ongoing maintenance of the existing wholesale sales website, and the design and
      implementation of a retail sales website to expand our customer reach.`,
    jobAddress: 'Caracas / Venezuela'
  },
  {
    timeWorked: 'May, 2019 – Feb, 2020',
    jobCompany: 'Backend Developer - Paxer',
    jobDescription: `I contributed to
      the enhancement of a hotel management software by developing new features and integrating it with
      top service providers like Expedia and Booking. Leveraging technologies like Java, RabbitMQ, and
      Docker, I built resilient and scalable systems, guaranteeing peak performance and modular design.
      Additionally, I automated reservation management and availability updates, streamlining processes
      and enhancing efficiency.`,
    jobAddress: 'Caracas / Venezuela'
  },
  {
    timeWorked: 'Feb, 2018 – Dic, 2018',
    jobCompany: 'Full Stack Developer - Jumperr',
    jobDescription: `During my
      tenure, I actively engaged in the design and development of web applications from inception,
      playing a pivotal role in crafting new features and functionalities for the product. Remaining
      abreast of cutting-edge technologies and trends in web development, I fostered diversified
      experience through a multitude of tasks and projects, accelerating my professional growth.
      Furthermore, I made substantial contributions to shaping the product's vision and strategy,
      solidifying my impact within the company.`,
    jobAddress: 'Caracas / Venezuela'
  },
  {
    timeWorked: 'Apr, 2017 – Feb, 2018',
    jobCompany: 'Backend Developer - Grupos de Empresas ITBC',
    jobDescription: `In my position, I actively contributed to the design and development of the company's
      intranet, while also playing a pivotal role in enhancing the Digitel client platform through 
      the development of new features. Additionally, I spearheaded the creation of innovative functionalities
      tailored to diverse clients in Spain. Notable achievements include obtaining certifications in Java 
      environments and Scrum methodologies, furthering my professional growth in Java and PHP technologies.`,
    jobAddress: 'Caracas / Venezuela'
  },
  {
    timeWorked: 'Aug, 2016 – Apr, 2017',
    jobCompany: 'Full Stack Developer - VACORP',
    jobDescription: `In my role at the company, I was tasked with implementing the Bootstrap framework 
      into the study management system, as well as developing the Create, Read, Update, and Delete (CRUD) 
      functionalities for student information management. 
      Additionally, I handled troubleshooting and bug fixing. My accomplishments included continuous
      learning and professional development, alongside effective collaboration with the development team.`,
    jobAddress: 'Caracas / Venezuela'
  }
]);
</script>

<style scoped>
@import '../css/experiences-component.css';
</style>