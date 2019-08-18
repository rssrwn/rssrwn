<template>
  <div id="page">
    <h2 class="subTitle">Projects</h2>
    <div id="projects">
      <div class="project">
        <div class="projectTitleAndText">
          <h2 class="projectTitle">Edubot</h2>
          <div class="projectText">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </div>
        </div>
        <div class="projectPicDiv">
          <img class="projectPic" src="../assets/Octocat.png"/>
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
  display: flex;
  justify-content: space-between;
}
.projectTitle {
  margin: 5px 0px 10px 0px;
}
.projectPicDiv {
  width: 100%;
}
.projectPic {
  width: 100%;
}
.projectTitleAndText {
  height: 100%;
}
</style>
