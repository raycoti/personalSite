<template>
  <div class="home">
    <h1>{{inputText}}</h1>
    <!-- {{images}} -->
    <ArtGallery :images="images" />
    <HelloWorld :message="inputText" />
    <input v-model="inputText"/>
  </div>
</template>

<script >
// @ is an alias to /src
import selfImg from '@/assets/self.png';
import soulImg from '@/assets/soulSearching.jpg';
import ArtGallery from '@/components/Art.vue';
import HelloWorld from '@/components/HelloWorld.vue';

export default {
  name: 'Home',
  components: {
    ArtGallery,
    HelloWorld,
  },
  data: () => ({
    images: [
      {
        src: selfImg,
        title: 'Self',
      },
      {
        src: soulImg,
        title: 'searching',
      },
    ],
    inputText: 'hi',
  }),
};
</script>
