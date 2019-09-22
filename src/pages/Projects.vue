<template>
  <div id="page">
    <h2 class="subTitle">Projects</h2>
    <div id="projects">
      <div class="project">
        <div class="projectTitle"><h2 class="projectTitle">EduBot</h2></div>
        <div>
          <div class="projectText">
            <p>Key Stage 3 students are now required to learn basic programming concepts, including looping, functions, sorting and searching. However, a lack of fully qualified Computing teachers has made it very difficult for some schools to meet the curriculum requirements. Which means many students are missing out on crucial programming education.</p>
            <p>We (a team of four) designed EduBot to help solve this problem. After being given a textual introduction to a programming concept students attempt to implement an algorithm using code blocks which will make a robot move around a level. The goal is make EduBot gather all the nuts and bolts in as few moves as possible. Each level provides the student with a new challenge and a new programming concept to master. The platform also provides teachers with the ability to track their students' progress and to give feedback to individual students on each level.</p>
            <p>EduBot ranked in the top 5 projects in our year group (out of over 40 projects) and our team was invited to present EduBot at the department's open day.</p>
          </div>
          <div class="projectPicDiv">
            <img class="projectPic" src="../assets/edubot.png"/>
          </div>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
  export default {
    name: "projects"
  }
</script>

<style scoped>
.subTitle {
  font-family: 'Merriweather', serif;
  font-size: 30px;
  font-weight: bold;
  border-bottom: 1px lightgrey solid;
  color: palevioletred;
}
.project {
  border: 1px lightgrey solid;
  border-radius: 10px;
  padding: 20px;
  display: block;
  margin: 40px 0px;
}
.projectTitle {
  margin: 5px 0px 10px 0px;
}
.projectPicDiv {
  width: 100%;
  display: flex;
  justify-content: center;
}
.projectPic {
  width: 75%;
  border: 1px lightgrey solid;
  border-radius: 5px;
}
</style>
