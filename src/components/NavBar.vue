<template>
  <div id="bar">
    <div id="nav">
      <div id="mainButton" class="circle large">
        <div id="barTitle">Ross</div>
      </div>
      <div id="childNodes">
        <div class="buttons left">
          <!--<div class="circle" id="homeCircle">-->
            <!--<div class="circleText">Home</div>-->
          <!--</div>-->
          <!--<svg style="" height="0" width="0" class="svg" id="homeSvg">-->
            <!--<line class="line" id="homeLine" x1="0" y1="0" x2="0" y2="0"></line>-->
          <!--</svg>-->
          <nav-node name="Home"></nav-node>
          <!--<div class="circle">-->
            <!--<div>About</div>-->
          <!--</div>-->
          <nav-node name="About"></nav-node>
        </div>
        <div class="buttons right">
          <!--<div class="circle">-->
            <!--<div>Projects</div>-->
          <!--</div>-->
          <nav-node name="Projects"></nav-node>
          <!--<div class="circle">-->
            <!--<div>CV</div>-->
          <!--</div>-->
          <nav-node name="CV"></nav-node>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import NavNode from "./NavNode";

  function centreOf(elem) {
    var cx = (elem.offsetWidth / 2) + elem.offsetLeft;
    var cy = (elem.offsetHeight / 2) + elem.offsetTop;
    return [cx, cy];
  }

  export default {
    name: "nav-bar",
    components: {NavNode},
    mounted: function() {
      this.$nextTick(function() {
        var mainButton = this.$el.childNodes[0].childNodes[0];
        var c2 = centreOf(mainButton);
        var cx2 = c2[0];
        var cy2 = c2[1];

        var homeCircle = document.getElementById("homeCircle");
        var c1 = centreOf(homeCircle);
        var cx1 = c1[0];
        var cy1 = c1[1];

        var width = cx2 - cx1;
        var height = cy1 - cy2;

        var svg = document.getElementById("homeSvg");
        svg.setAttributeNS(null, "style", "left:"+cx1+"px;top:"+cy2+"px");
        svg.setAttributeNS(null, "width", width);
        svg.setAttributeNS(null, "height", height);

        var line = document.getElementById("homeLine");
        line.setAttributeNS(null, "x1", 0);
        line.setAttributeNS(null, "x2", width);
        line.setAttributeNS(null, "y1", height);
        line.setAttributeNS(null, "y2", 0);
      })
    }
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

.circleText {
  z-index: 2;
}

#barTitle {
  font-family: 'Lobster Two', cursive;
  color: palevioletred;
  font-size: 60px;
  font-weight: bold;
}

.svg {
  position: absolute;
  z-index: 0;
}

.line {
  stroke: #2c3e50;
  stroke-width: 3px;
  z-index: 0;
}
</style>
