<template>
  <div id="app">
    <Home></Home>
  </div>
</template>

<script>
import Home from './components/home'

export default {
  name: 'App',
  components: {
    Home
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
}
.main {
  max-width: 1280px;
  margin: 0 auto;
}
</style>
