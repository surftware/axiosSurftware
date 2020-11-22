<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg2='El Jose' msg="Welcome to Your Vue.js App"/>
    <HelloSurftware msg2='Surf' msg="Hola mundo"/>
    <firstAxios msg2='Surf' msg="Hola mundo" />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HelloSurftware from './components/surftware.vue'
import firstAxios from './components/axios.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    HelloSurftware,
    firstAxios
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
