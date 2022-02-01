<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

  <ArrayVue />
  <ReduceVue />
  <FindVue />
  <FilterVue />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import ArrayVue from './pages/array.vue'
import ReduceVue from './pages/reduce.vue'
import FindVue from './pages/find.vue'
import FilterVue from './pages/filter.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld, 
    ArrayVue,
    ReduceVue,
    FindVue,
    FilterVue
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


