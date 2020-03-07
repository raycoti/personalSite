<template>
    <div>
        <div v-for="image in images" :key="image.src" >
            <img :src="image.src" />
        </div>
    </div>
</template>

<script >

export default {
  name: 'ArtGallery',
  props: {
    images: Array,
  },
};

</script>
