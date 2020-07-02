<template>
  <div id="app">
    <nav-bar></nav-bar>
    <div id="frame">
      <projects></projects>
    </div>
    <contact-footer></contact-footer>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import ContactFooter from "./components/ContactFooter";
import Projects from './pages/Projects'

export default {
  name: 'app',
  components: {
    NavBar,
    ContactFooter,
    Projects
  }
}
</script>

<style>
#app {
  font-family: Nunito, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#frame {
  margin: 100px 100px;
}

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
</style>
