<template>
  <div class="about">
    <div class="center">
      <div class="container">
        <div class="grid">
          <span>
            <img class="picture" :src="Ray" />
          </span>
          <span>

          <p> Ray is ... </p>
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
  max-width: 90rem;
  padding: 1rem 4rem;
}
.picture{
  border-radius: 100%;
  width: 100%;
}
.grid{
  display: grid;
  grid-template-columns: 1fr 5fr;
  p{
    max-width: 50rem;
    padding-left: 1rem;
    text-align: left;
  }
}
</style>
