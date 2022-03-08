<template>
  <HomePage />
</template>

<script>
import HomePage from './views/HomePage.vue';

export default {
  name: 'App',
  components: {
    HomePage
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
  height: 100vh!important;
  margin-left: 2%;
  margin-right: 2%;
  margin-top: 1%;
  position: fixed;
  width: -webkit-fill-available;
}
</style>
