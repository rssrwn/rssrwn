<template>
  <div id="app">
    <nav-bar></nav-bar>
    <div id="frame">
      <router-view></router-view>
    </div>
    <contact-footer></contact-footer>
  </div>
</template>

<script>
  import ContactFooter from "./components/ContactFooter";
  import NavBar from "./components/NavBar";
  export default {
    components: {NavBar, ContactFooter}
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
  margin: 100px 150px;
}
</style>
