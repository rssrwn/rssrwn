<!--<template>-->
  <!--<div id="bar">-->
    <!--<div id="nav">-->
      <!--<div class="buttons">-->
        <!--<div class="circle">-->
          <!--<div><h3>Home</h3></div>-->
        <!--</div>-->
        <!--<div class="circle">-->
          <!--<div><h3>About</h3></div>-->
        <!--</div>-->
      <!--</div>-->
      <!--<div class="circle large">-->
        <!--<div id="barTitle">Ross</div>-->
      <!--</div>-->
      <!--<div class="buttons">-->
        <!--<div class="circle">-->
          <!--<div><h3>Projects</h3></div>-->
        <!--</div>-->
        <!--<div class="circle">-->
          <!--<div><h3>CV</h3></div>-->
        <!--</div>-->
      <!--</div>-->
    <!--</div>-->
  <!--</div>-->
<!--</template>-->

<template>
  <div id="bar">
    <div id="nav">
      <div id="mainButton" class="circle large">
        <div id="barTitle">Ross</div>
      </div>
      <div id="childNodes">
        <div class="buttons left">
          <div class="circle">
            <div>Home</div>
          </div>
          <div class="circle">
            <div>About</div>
          </div>
        </div>
        <div class="buttons right">
          <div class="circle">
            <div>Projects</div>
          </div>
          <div class="circle">
            <div>CV</div>
          </div>
        </div>
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
  width: available;
  background-color: white;
  display: flex;
  align-items: center;
}

#nav {
  display: inline;
  width: 100%;
  margin-top: -100px;
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
  margin-top: -80px;
}

.buttons {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: space-evenly;
  /*margin: 0px 80px;*/
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
}
.circle.large {
  height: 300px;
  width: 300px;
}

#barTitle {
  font-family: 'Lobster Two', cursive;
  color: palevioletred;
  font-size: 60px;
  font-weight: bold;
}
</style>
