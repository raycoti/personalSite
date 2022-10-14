<template>
  <!-- <transition> -->
    <div class="projects">
      <div class="center">
        <div
          class="header"
          :style="{backgroundImage: `url(${header})`}">
          <div>
            <h1>Projects</h1>
          </div>
        </div>
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
    </div>
  <!-- </transition> -->
</template>

<style scoped lang="scss">
@import './Projects.scss';
</style>

<script>
import Project from '@/components/Project.vue';
import IN from '@/assets/projects/project.png';
import Soul from '@/assets/pics/soulSearching.jpg';

export default {
  name: 'Projects',
  components: {
    Project,
  },
  data: () => ({
    header: Soul,
    projects: [
      {
        src: IN,
        title: 'Inveractive Narrative',
        description: `
        This is an ART CAPSTONE PROJECT I made during the 2015-2016 academic year.
        In this piece, I wanted to portray how labels contributed to feeling out of place during college.
        The project was built using Unity 3D, Maya3D, and Blender.`,
        link: 'https://interactivenarrative.azurewebsites.net/',
      },
    ],
  }),
};
</script>
