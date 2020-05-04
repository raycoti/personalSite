<template>
  <div class="home">
    <Nav />
    <ArtGallery :gridId="gridId" :images="images" />
  </div>
</template>

<script >
// @ is an alias to /src
import soulImg from '@/assets/soulSearching.jpg';
import selfImg from '@/assets/self.png';
import fish from '@/assets/fish.png';
import desk from '@/assets/desk.png';
import shell from '@/assets/shell.png';
import searchin from '@/assets/searchin.png';
import untitled from '@/assets/Untitled.png';
import tree from '@/assets/tree.png';
import robot from '@/assets/arm.png';
import bridge from '@/assets/bridge.png';
import city from '@/assets/city.jpg';
import turtle from '@/assets/turtle.png';
import kite from '@/assets/kite.png';
import kite2 from '@/assets/ite.jpg';
import existence from '@/assets/existence.jpg';
import ArtGallery from '@/components/Art.vue';
import Nav from '@/components/Nav.vue';

export default {
  name: 'Art',
  components: {
    ArtGallery,
    Nav,
  },
  data: () => ({
    gridId: 'artGrid',
    images: [
      {
        src: selfImg,
        title: 'Self',
      },
      {
        src: fish,
        title: 'fish',
      },
      {
        src: desk,
        title: 'Desk',
      },
      {
        src: searchin,
        title: 'searching2',
      },
      {
        src: tree,
        title: 'treee',
      },
      {
        src: untitled,
        title: 'nightmare',
      },
      {
        src: shell,
        title: 'shell',
      },
      {
        src: soulImg,
        title: 'soul',
      },
      {
        src: turtle,
        title: 'turtle',
      },
      {
        src: robot,
        title: 'robot',
      },
      {
        src: bridge,
        title: 'bridge',
      },
      {
        src: city,
        title: 'city',
      },
      {
        src: kite2,
        title: 'kite2',
      },
      {
        src: kite,
        title: 'kite',
      },
      {
        src: existence,
        title: 'existence',
      },
    ],
  }),
};
</script>

<style lang="scss">
@import url('./Art.scss')
</style>
