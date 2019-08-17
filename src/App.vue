<template>
  <div id="app">
    <nav-bar></nav-bar>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";

export default {
  name: 'app',
  components: {
    NavBar
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

/*
font-family: 'Merriweather', serif;
font-family: 'Lobster', cursive;
font-family: 'Vollkorn', serif;
font-family: 'Lobster Two', cursive;
font-family: 'Alice', serif;
font-family: 'Press Start 2P', cursive;
font-family: 'Noto Serif', serif;
font-family: 'Noto Sans', sans-serif;
*/
}
</style>
