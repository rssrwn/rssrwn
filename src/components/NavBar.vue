<template>
  <div id="bar">
    <div id="nav">
      <div id="mainButton" class="circle large">
        <div id="barTitle">Ross</div>
      </div>
      <div id="childNodes">
        <div class="buttons left">
          <router-link to="/">
            <nav-node name="Home"></nav-node>
          </router-link>
          <router-link to="/about">
            <nav-node name="About"></nav-node>
          </router-link>
        </div>
        <div class="buttons right">
          <router-link to="/projects">
            <nav-node name="Projects"></nav-node>
          </router-link>
          <router-link to="cv">
            <nav-node name="CV"></nav-node>
          </router-link>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import NavNode from "./NavNode";

  export default {
    name: "nav-bar",
    components: {NavNode}
  }
</script>

<style scoped>
#bar {
  width: available;
  background-color: white;
  display: flex;
  align-items: center;
}

#nav {
  display: inline;
  width: 100%;
  margin-top: -150px;
  margin-left: 100px;
  margin-right: 100px;
}

#mainButton {
  margin: auto;
}

#childNodes {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  color: #2c3e50;
  font-family: Oswald, sans-serif;
  font-size: 28px;
  width:100%;
  margin-top: -100px;
}

.buttons {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-evenly;
}
.buttons.left {
  margin-right: 120px;
}
.buttons.right {
  margin-left: 120px;
}

.circle {
  height: 150px;
  width: 150px;
  border-radius: 50%;
  border: 3px solid #2c3e50;
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: whitesmoke;
  z-index: 1;
  position: relative;
}
.circle.large {
  height: 300px;
  width: 300px;
  background-color: whitesmoke;
  z-index: 1;
}

#barTitle {
  font-family: 'Lobster Two', cursive;
  color: palevioletred;
  font-size: 60px;
  font-weight: bold;
  margin-top: 100px;
}
</style>
