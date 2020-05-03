<template>
  <transition name="fade">
    <div class="container">
      <div class="white">
        <h1>Ray Coti</h1>
        <h2>Blurring the line between dreams and reality</h2>
        <router-link class="enter" to="/art">ENTER</router-link>
      </div>
    </div>
  </transition>
</template>

<style scoped lang="scss">
@import './Home.scss';
</style>

<script>
export default {
  name: 'Home',
};
</script>
