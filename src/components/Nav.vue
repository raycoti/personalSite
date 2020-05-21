<template>
    <div id="nav">
      <router-link v-on:click.native="onClick" to="/about">About</router-link> |
      <router-link v-on:click.native="onClick" to="/art">Art</router-link> |
      <router-link v-on:click.native="onClick" to="/projects">Projects</router-link>
    </div>
</template>

<script>
export default {
  methods: {
    onClick: () => {
      window.scrollTo(0, 0);
    },
  },
};
</script>
