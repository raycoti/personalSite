<template>
  <div class="about">
    <div class="center">
      <div class="container">
        <div class="grid">
          <span>
            <img class="picture" :src="Ray" />
          </span>
          <span>

          <p> A Full-Stack Developer who loves to use technology to blur the line
            between dreams and reality.
            Ray prides himself in being a leader and mentor </p>
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

import Ray from '@/assets/ray.jpg';

export default {
  name: 'About',
  data: () => ({
    Ray,
  }),
};
</script>
<style scoped lang="scss">
.container{
  margin-top: 5rem;
  color: #3C3F40;
  max-width: 100rem;
}
.picture{
  border-radius: 100%;
  width: 100%;
}
.grid{
  display: grid;
  grid-template-columns: 1fr 5fr;
}
</style>
