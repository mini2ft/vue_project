<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  <ArrayVue />
  <ReduceVue />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ArrayVue from './pages/array.vue'
import ReduceVue from './pages/reduce.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld, 
    ArrayVue,
    ReduceVue
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


