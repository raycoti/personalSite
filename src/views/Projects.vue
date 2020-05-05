<template>
  <!-- <transition> -->
    <div class="projects">
      <Nav />
      <div class="container">
        <Project
          v-for="project in projects"
          :key="project.src"
          :project="project"
        />
      </div>
    </div>
  <!-- </transition> -->
</template>

<style scoped lang="scss">
.container{
  width: 100%;
  margin-top: 5rem;
  display: grid;
  grid-gap: 1rem;
  grid-template-columns: repeat(2, 1fr);
  // grid-template-rows: repeat(2, 1fr);
}
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
      },
      {
        src: OFN,
        title: 'Openfinance',
      },
    ],
  }),
};
</script>
