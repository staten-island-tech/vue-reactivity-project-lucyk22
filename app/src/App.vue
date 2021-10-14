<template>
  <div id="app">
    <HelloWorld dialogue="HI  EVERY  !
    "/>
  </div>
</template>

<script>
import HelloWorld from './components/Spamton.vue'

export default {
  name: 'App',
  components: {
    Spamton
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
