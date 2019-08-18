<template>
  <div id="bar">
    <div id="nav">
      <div class="buttons">
        <div><h3>Home</h3></div>
        <div><h3>About</h3></div>
      </div>
      <div id="barTitle">Ross</div>
      <div class="buttons">
        <div><h3>Projects</h3></div>
        <div><h3>CV</h3></div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "nav-bar"
  }
</script>

<style scoped>
#bar {
  height: 100px;
  width: available;
  background-color: white;
  display: flex;
  align-items: center;
  border-bottom: 1px lightgrey solid;
}
#nav {
  display: flex;
  width: 100%;
  justify-content: space-evenly;
}
.buttons {
  width: 20%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #2c3e50;
  font-family: 'Noto Serif', serif;
  font-size: 18px;
  font-weight: bold;
}
#barTitle {
  font-family: 'Lobster Two', cursive;
  color: palevioletred;
  font-size: 60px;
  font-weight: bold;
  text-align: center;
  justify-content: center;
  line-height: 100px;
}
</style>
