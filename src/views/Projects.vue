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
        title: 'Inveractive Narrative 2016',
        description: `
        This project is a “walking simulator” that takes players on my journey as a first-generation student 
        travelling away for college. The story is told through interactable snippets and visual metaphors.
        The project was originally built with multiple users in mind (via networking and matchmaking) 
        and I used that to disrupt the control of my own narrative. I did this by having the snippets cycle 
        one sentence at a time, rather than be shown in full. This meant that the last sentence a user 
        reads, would become the first sentence the next user reads. Thus, as more people interact with the
        environment the more mixed up the story would become.  
        The project was built using Unity 3D, Maya3D, and Blender.
        `,
        link: 'https://interactivenarrative.azurewebsites.net/',
      },
    ],
  }),
};
</script>
