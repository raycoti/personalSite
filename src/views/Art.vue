<template>
  <div class="home">
    <ArtGallery :gridId="gridId" :images="images" />
  </div>
</template>

<script >
// @ is an alias to /src
import soulImg from '@/assets/pics/soulSearching.jpg';
import selfImg from '@/assets/pics/self.png';
import fish from '@/assets/pics/fish.png';
import desk from '@/assets/pics/desk.png';
import shell from '@/assets/pics/shell.png';
import searchin from '@/assets/pics/searchin.png';
import untitled from '@/assets/pics/Untitled.png';
import tree from '@/assets/pics/tree.png';
import robot from '@/assets/pics/arm.png';
import bridge from '@/assets/pics/bridge.png';
import city from '@/assets/pics/city.jpg';
import turtle from '@/assets/pics/turtle.png';
import kite from '@/assets/pics/kite.png';
import kite2 from '@/assets/pics/ite.jpg';
import existence from '@/assets/pics/existence.jpg';
import moon from '@/assets/pics/moon.png';
import forest from '@/assets/pics/forest.png';
import spiral from '@/assets/pics/spiral.jpg';
import pallet from '@/assets/pics/pallets.png';
import ArtGallery from '@/components/Art.vue';

export default {
  name: 'Art',
  components: {
    ArtGallery,
  },
  methods: {
    lazyLoad() {
      const ref = this.lazyLoad;
      let lazyImages = [].slice.call(document.querySelectorAll('img.lazy'));
      let active = false;
      if (active === false) {
        active = true;
        setTimeout(() => {
          lazyImages.forEach((lazyImage) => {
            if ((lazyImage.getBoundingClientRect().top <= window.innerHeight && lazyImage.getBoundingClientRect().bottom >= 0) && getComputedStyle(lazyImage).display !== 'none') {
              // eslint-disable-next-line no-param-reassign
              lazyImage.src = lazyImage.dataset.src ? lazyImage.dataset.src : '';
              lazyImage.classList.remove('lazy');
              lazyImages = lazyImages.filter((image) => image !== lazyImage);
              if (lazyImages.length === 0) {
                window.removeEventListener('scroll', ref);
              }
            }
          });
          active = false;
        }, 200);
      }
    },
  },
  created() {
    window.addEventListener('scroll', this.lazyLoad);
    setTimeout(() => {
      window.scrollTo(0, 1);
    }, 100);
  },
  destroyed() {
    window.removeEventListener('scroll', this.lazyLoad);
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
      {
        src: moon,
        title: 'moon',
      },
      {
        src: forest,
        title: 'forest',
      },
      {
        src: spiral,
        title: 'spiral',
      },
      {
        src: pallet,
        title: 'pallet',
      },
    ],
  }),
};
</script>

<style lang="scss">
@import './Art.scss';
</style>
