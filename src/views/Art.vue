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
        style: {
          gridArea: 'self',
        },
      },
      {
        src: fish,
        title: 'nightmare',
        style: {
          gridArea: 'fish',
        },
      },
      {
        src: desk,
        title: 'Desk',
        style: {
          gridArea: 'desk',
        },
      },
      {
        src: searchin,
        title: 'searching 2',
        style: {
          gridArea: 'searching',
        },
      },
      {
        src: tree,
        title: 'treee',
        style: {
          gridArea: 'tree',
          paddingTop: '1rem',
        },
      },
      {
        src: untitled,
        title: 'nightmare',
        style: {
          gridArea: 'nightmare',
        },
      },
      {
        src: shell,
        title: 'shell',
        style: {
          gridArea: 'shell',
        },
      },
      {
        src: soulImg,
        title: 'soul',
        style: {
          gridArea: 'soul',
        },
      },
      {
        src: turtle,
        title: 'turtle',
        style: {
          gridArea: 'turtle',
        },
      },
      {
        src: robot,
        title: 'robot',
        style: {
          gridArea: 'arm',
        },
      },
      {
        src: bridge,
        title: 'bridge',
        style: {
          gridArea: 'bridge',
        },
      },
      {
        src: city,
        title: 'city',
        style: {
          gridArea: 'city',
        },
      },
      {
        src: kite2,
        title: 'kite2',
        style: {
          gridArea: 'kite2',
        },
      },
      {
        src: kite,
        title: 'kite',
        style: {
          gridArea: 'kite',
        },
      },
      {
        src: existence,
        title: 'existence',
        style: {
          gridArea: 'existence',
        },
      },
    ],
    inputText: 'hi',
  }),
};
</script>
<style lang="scss">
@import url('./Art.scss')
</style>
