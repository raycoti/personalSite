<template>
  <div
    @click="open"
    class="project"
    :style="{backgroundImage: 'url('+ project.src + ')'}"
  >
    <div class="des">
      <h1 >{{project.title}}</h1>
    </div>
    <transition name="fade-overlay">
      <div class="overlay" @click="close" v-if="display">
        <div class="contianer">
          <div class="imageContainer" :style="{backgroundImage: `url(${project.src})`}">
          </div>
          <div>
            <h1>{{project.title}}</h1>
            <p>{{project.description}}</p>
            <button
              class="check"
              :v-if="project.link"
              @click="goTo(project.link, $event)">GO </button>
          </div>
        </div>
      </div>
    </transition>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

interface ProjectItem {
  src: string;
  description?: string;
  link?: string;
  title?: string;
}

@Component
export default class Project extends Vue {
  @Prop() private project!: ProjectItem;

  display = false;

  open() {
    this.display = true;
  }

  close(e: Event) {
    e.stopPropagation();
    this.display = false;
  }

  goTo(link: string, e: Event) {
    e.stopPropagation();
    window.open(link);
    this.display = true;
  }
}

</script>

<style scoped lang="scss">
@import './Project.scss';
</style>
