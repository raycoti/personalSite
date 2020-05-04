<template>
  <div class="home">
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
import ArtGallery from '@/components/Art.vue';
import robot from '@/assets/arm.png';
import bridge from '@/assets/bridge.png';
import city from '@/assets/city.jpg';
import turtle from '@/assets/turtle.png';
import kite from '@/assets/kite.png';
import kite2 from '@/assets/ite.jpg';
import existence from '@/assets/existence.jpg';

export default {
  name: 'Art',
  components: {
    ArtGallery,
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
#artGrid{
  display: grid;
  grid-template-columns: repeat(8, 1fr);
  grid-gap: 5px;
  padding: 0;
  grid-template-areas:
    'tree tree tree soul soul soul soul soul'
    'tree tree tree soul soul soul soul soul'
    'tree tree tree fish fish fish searching searching'
    'tree tree tree fish fish fish searching searching'
    'desk desk desk fish fish fish bridge kite'
    'desk desk desk self self shell shell shell '
    'desk desk desk self self shell shell shell '
    'turtle turtle nightmare nightmare nightmare shell shell shell '
    'turtle turtle nightmare nightmare nightmare city city city'
    'kite2 kite2 arm arm arm city city city'
    'existence existence arm arm arm city city city'
    'existence existence . . . city city city';
    // '. . . . . . . . .';
}

/*
  grid-template-areas:
    'tree tree tree self self . soul soul soul'
    'tree tree tree self self . soul soul soul'
    'tree tree tree fish searching nightmare . . .'
    'tree tree tree . . . . . .';
    // '. . . . . . . . .';
}
*/
</style>
