<template>
  <div>
    <div class="circle">
      <div class="circleText">{{ name }}</div>
    </div>
    <svg style="" height="0" width="0" class="svg">
      <line class="line" x1="0" y1="0" x2="0" y2="0"></line>
    </svg>
  </div>
</template>

<script>
  function centreOf(elem) {
    let cx = (elem.offsetWidth / 2) + elem.offsetLeft;
    let cy = (elem.offsetHeight / 2) + elem.offsetTop;
    return [cx, cy];
  }

  export default {
    name: "NavNode",
    props: ["name"],

    mounted: function() {
      this.$nextTick(function() {
        let mainButton = document.getElementById("mainButton");
        let c2 = centreOf(mainButton);
        let cx2 = c2[0];
        let cy2 = c2[1];

        let circle = this.$el.childNodes[0];
        let c1 = centreOf(circle);
        let cx1 = c1[0];
        let cy1 = c1[1];

        let width = cx2 - cx1;
        let height = cy1 - cy2;

        let svg = this.$el.childNodes[1];
        svg.setAttributeNS(null, "style", "left:"+cx1+"px;top:"+cy2+"px");
        svg.setAttributeNS(null, "width", width);
        svg.setAttributeNS(null, "height", height);

        let line = svg.childNodes[0];
        line.setAttributeNS(null, "x1", "0");
        line.setAttributeNS(null, "x2", width);
        line.setAttributeNS(null, "y1", height);
        line.setAttributeNS(null, "y2", "0");
      })
    }
  }
</script>

<style scoped>
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

  .circleText {
    z-index: 2;
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
