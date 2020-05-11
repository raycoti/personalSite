<template>
  <!-- <transition> -->
    <div class="projects">
      <Nav />
      <div class="p-container">
        <div class="container">
          <Project
            v-for="project in projects"
            :key="project.src"
            :project="project"
          />
        </div>
      </div>
    </div>
  <!-- </transition> -->
</template>

<style scoped lang="scss">
@import './Projects.scss';
</style>

<script>
import Nav from '@/components/Nav.vue';
import Project from '@/components/Project.vue';
import IN from '@/assets/projects/project.png';
import OFN from '@/assets/projects/ofn.png';

export default {
  name: 'Projects',
  components: {
    Nav,
    Project,
  },
  data: () => ({
    projects: [
      {
        src: IN,
        title: 'Inveractive Narrative',
        description: `
        This is an ART CAPSTONE PROJECT I made during the 2015-2016 academic year.
        In this piece I wanted to portray how labels contributed to feeling out of place during college.
        The project was built using Unity 3D, Maya3D and Blender.`,
        link: 'https://interactivenarrative.azurewebsites.net/',
      },
      {
        src: OFN,
        title: 'Openfinance',
        description: `
        As a Software Developer at OPENFINANCE , I lead a team through the creation of the WEB APPLICATION for our platform, the first ever to trade security tokens.
        It is written using React, Redux and Typescript.`,
        link: 'https://app.openfinance.io/',
      },
    ],
  }),
};
</script>
