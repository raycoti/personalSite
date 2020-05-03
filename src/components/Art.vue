<template>
  <span>
    <div :id="gridId" class="grid"  >
      <div
        v-for="image in images"
        :key="image.src"
        :style="image.style"
        @click="setDisplay(image.src)" >
          <img :src="image.src" />
      </div>
    </div>
    <transition name="fade-overlay">
      <div class="overlay" @click="close" v-if="display">
        <div class="imageContainer">
          <img :src="modalImg" />
        </div>
      </div>
    </transition>
  </span>
</template>

<script lang="ts">

import { Component, Prop, Vue } from 'vue-property-decorator';

interface ArtItem {
  src: string;
  title?: string;
  style?: unknown;
}

@Component
export default class ArtGaller extends Vue {
  @Prop() private images!: ArtItem[];

  @Prop() private gridId?: string;

  display = false;

  modalImg = '';

  setDisplay(src: string) {
    this.display = true;
    this.modalImg = src;
  }

  close() {
    this.display = false;
  }
}

</script>

<style scoped lang="scss">
@import './Art.scss';
</style>
