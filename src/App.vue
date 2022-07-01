<template>
  <div>
    <HomePage/>
  </div>
</template>

<script>
import HomePage from './components/Home.vue'
export default {
  name: 'App',
  components: {
    HomePage,
  }
}
</script>

<style scoped>
div{
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  background-color: black;
}
</style>
