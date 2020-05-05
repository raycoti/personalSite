<template>
  <div class="project"
    :style="{backgroundImage: 'url('+ project.src + ')'}"
  >
  <div>
    <h1>{{project.title}}</h1>
  </div>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

interface ProjectItem {
  src: string;
  title?: string;
  description?: unknown;
}

@Component
export default class Project extends Vue {
  @Prop() private project!: ProjectItem;
}

</script>

<style scoped lang="scss">
.project{
  // width: 100%;
  // max-width: 40rem;
  // max-height: 40rem;
  background-position: center;
  background-size: cover;
  min-height: 25rem;
  width: 100%;
  display: flex;
  div{
    width: 100%;
    margin-top: auto;
    background-color: black;
    h1{
      color: #ffffff;
  }
  }
}
</style>
