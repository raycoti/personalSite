<template>
  <div id="app">
    <Nav v-if="shouldRender" />
    <router-view/>
  </div>
</template>

<style lang="scss">
@import './common.scss';
</style>

<script>
import Nav from '@/components/Nav.vue';

export default {
  components: {
    Nav,
  },
  computed: {
    shouldRender() {
      return this.$route.name !== undefined;
    },
  },
};
</script>
