<template>
  <div id="app">
    <!--<div id="nav">-->
      <!--<router-link to="/">Home</router-link> |-->
      <!--<router-link to="/about">About</router-link>-->
    <!--</div>-->
    <nav-bar></nav-bar>
    <router-view>
      <div id="frame">
        <projects></projects>
      </div>
    </router-view>
    <contact-footer></contact-footer>
  </div>
</template>

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
<script>
  import Projects from "./views/Projects";
  import ContactFooter from "./components/ContactFooter";
  import NavBar from "./components/NavBar";
  export default {
    components: {NavBar, ContactFooter, Projects}
  }
</script>
