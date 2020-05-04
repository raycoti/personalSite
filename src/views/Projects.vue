<template>
  <transition>
    <div class="projects">
      <Nav />
      <div class="container">
        <h1>my projects</h1>
      </div>
    </div>
  </transition>
</template>

<style scoped lang="scss">
.container{
  margin-top: 5rem;
}
</style>

<script>
import Nav from '@/components/Nav.vue';

export default {
  name: 'Projects',
  components: {
    Nav,
  },
};
</script>
