<template>
  <div id="bar">
    <div id="nav">
      <div class="buttons">
        <div><h3>Home</h3></div>
        <div><h3>About</h3></div>
      </div>
      <div class="circle"><div id="circleText"><h1>Ross</h1></div></div>
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
  height: 50px;
  width: available;
  background-color: #2c3e50;
  display: flex;
  align-items: center;
  margin-bottom: 100px;
}
#nav {
  display: flex;
  width: 100%;
  justify-content: space-evenly;
  margin: 5px 50px;
}
.buttons {
  width: 20%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: auto 50px;
  color: white;
}
.circle {
  width: 400px;
  height: 200px;
  background-color: #2c3e50;
  color: white;
  border-bottom-left-radius: 200px;
  border-bottom-right-radius: 200px;
  transform: translate(0px, 10px);
  display: flex;
  align-items: center;
  justify-content: center;
}
#circleText {
  position: relative;
  top: 20px;
  font-size: 30px;
}
</style>
