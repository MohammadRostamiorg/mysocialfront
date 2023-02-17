<template>

  <!-- <HelloWorld msg="Welcome to Your Vue.js App"> -->
    <HomePage></HomePage>

</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    HomePage
  }
}
</script>

<style>
@import url('assets/css/main.css');
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: #0C2840;
  padding: 20px;

}
</style>
