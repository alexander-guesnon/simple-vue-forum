<script>
  import Forum from './components/Forum.vue'

  export default {
    name: 'App',
    components: {
      Forum
    }
  }
</script>

<template>
  <div id="app">
   <Forum>Welcome to the Forum</Forum>
  </div>
</template>



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
