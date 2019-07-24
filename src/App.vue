<template>
  <div id="app">
    <Picture/>
  </div>
</template>

<script>
import Picture from './components/Picture'

export default {
  name: 'App',
  components: {
    Picture
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
