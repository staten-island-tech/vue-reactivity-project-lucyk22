<template>
  <div id="app">
    <Spamton dialogue="pain
    "/>
    <Shop />
  </div>
</template>

<script>
import Spamton from './components/Spamton.vue'
import Shop from './components/Store.vue'

export default {
  name: 'App',
  components: {
    Spamton,
    Shop
  }
}
</script>

<style>
html,body {
    background-color:black;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display:flex;
}
</style>
