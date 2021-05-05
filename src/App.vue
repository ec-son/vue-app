<template>
  <div id="app">
    <div class="header">
      <Header/>
      <NavLink/>
    </div>
    <div class="body">
      <router-view/>
    </div>
  </div>
</template>

<script>
import NavLink from "./views/NavLink.vue"
import Header from "./views/Header.vue"
  export default {
    name: "app",
    components: {
    NavLink,
    Header
  },
  }
</script>

<style lang="scss" scoped>
 .nav {
    font-family: sans-serif;
    display: flex;
    justify-content: space-around;
  }
  .body {
    max-width: 80%;
    margin: auto;
  }
</style>