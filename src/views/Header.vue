<template>
  <div class="header">
    <h3>Yotta e-commerce</h3>
  </div>
</template>

<script lang="ts">
  import { Options, Vue } from 'vue-class-component'
  @Options({
  components: {
  },
})
  export default class Header extends Vue {

  }
</script>

<style lang="scss" scoped>
  .header {
    background-color: rgb(37, 104, 37);
    padding: 1rem;
    h3 {
      text-align: center;
      font-weight: bold;
      color: white;
    }
  }
</style>