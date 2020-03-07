<template>
    <div>
        <div v-for="image in images" :key="image.src" >
            <img :src="image.src" />
        </div>
    </div>
</template>

<script lang="ts">

import { Component, Prop, Vue } from 'vue-property-decorator';

interface ArtItem {
  src: string;
  title?: string;
}

@Component
export default class ArtGaller extends Vue {
  @Prop() private images!: ArtItem[];
}

</script>
