<template>
  <div id="app">
    <LoadImage />
  </div>
</template>

<script>
import LoadImage from './components/LoaderImage.vue'
export default {
  name: 'App',
  components: {
    LoadImage
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
