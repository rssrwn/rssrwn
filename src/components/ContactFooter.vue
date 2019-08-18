<template>
  <div id="footer">
    <div id="footerHeader">Ross Irwin</div>
    <div id="contactList">
      <div class="contactTab"><a href="https://github.com/rssrwn"><img class="contactImage" src="../assets/Octocat.png" alt="GitHub Link"/></a></div>
      <div class="contactTab"><a href="https://www.linkedin.com/in/rssrwn"><img class="contactImage" src="../assets/LI-In-Bug.png" alt="LinkedIn Link"/></a></div>
      <div class="contactTab"><a id="emailLink" href="mailto:rssrwn@gmail.com"><div id="emailContact">@</div></a></div>
    </div>
  </div>
</template>

<script>
  export default {
    name: "contact-footer"
  }
</script>

<style scoped>
#footer {
  height: 180px;
  width: 100%;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  background-color: #f5f5f5;
}
#footerHeader {
  font-family: 'Lobster Two', cursive;
  color: grey;
  font-weight: bold;
  font-size: 36px;
  padding: 38px 50px;
}
#contactList {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  font-size: 18px;
  padding: 30px 30px;
  margin-right: 20px;
}
.contactTab {
  display: flex;
  align-items: center;
}
.contactImage {
  width: 50px;
  margin: 0px 20px;
}
#emailContact {
  font-size: 40px;
  font-weight: bold;
  width: 50px;
  height: 50px;
  margin: 0px 20px 0px 10px;
}
#emailLink {
  text-decoration: none;
  color: #2c3e50;
  padding-bottom: 5px;
}
</style>
