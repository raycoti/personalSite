<template>
  <div id="app">
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100%;
}

html, body {
  height: 100%;
  margin: 0;
}

#nav {
  a {
    font-weight: bold;
    color: #2c3e50;
    padding: 0 5px;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
  height: 5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  position:fixed;
  background-color: #ffffff;
  top: 0;
  z-index: 5;
}
</style>
