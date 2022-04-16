<template>
<!-- <div id="app">
<p>You clicked {{ numOfClicks }} times.</p>
<button @click="handleClick()">Click me to increment!</button>
</div> -->

  <!-- <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <Menu msg="Welcome to Your Vue.js App"/>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Menu from './components/menu.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld,
    Menu,
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

