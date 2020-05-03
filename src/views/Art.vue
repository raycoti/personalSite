<template>
  <div class="home">
    <ArtGallery :gridId="gridId" :images="images" />
  </div>
</template>

<script >
// @ is an alias to /src
// import soulImg from '@/assets/soulSearching.jpg';
import selfImg from '@/assets/self.png';
import fish from '@/assets/fish.png';
import desk from '@/assets/desk.png';
import shell from '@/assets/shell.png';
import searchin from '@/assets/searchin.png';
import untitled from '@/assets/Untitled.png';
import tree from '@/assets/tree.png';
import ArtGallery from '@/components/Art.vue';

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
    ],
    inputText: 'hi',
  }),
};
</script>
<style lang="scss">
#artGrid{
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-gap: 5px;
  max-width: 99vw;
  padding: 0;
  grid-template-areas:
    'tree tree tree self self desk'
    'tree tree tree self self shell'
    'tree tree tree fish nightmare searching'
    'tree tree tree . . .';
}
</style>
