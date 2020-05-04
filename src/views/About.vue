<template>
  <div class="about">
    <Nav />
    <div class="container">
      <h1>Ray Coti is..</h1>
    </div>
  </div>
</template>

<script>

import Nav from '@/components/Nav.vue';

export default {
  name: 'About',
  components: {
    Nav,
  },
};
</script>
<style scoped lang="scss">
.container{
  margin-top: 5rem;
}
</style>
