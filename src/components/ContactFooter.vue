<template>
  <div id="footer">
    <div id="footerHeader">Ross Irwin</div>
    <div id="contactList">
      <div class="contactTab"><a href="https://github.com/rssrwn"><img class="contactImage" src="../assets/github-icon.png" alt="GitHub Link"/></a></div>
      <div class="contactTab"><a href="https://www.linkedin.com/in/rssrwn"><img class="contactImage" src="../assets/linkedin-icon.png" alt="LinkedIn Link"/></a></div>
      <div class="contactTab"><a id="emailLink" href="mailto:rssrwn@gmail.com"><img class="contactImage" src="../assets/email-icon-open.png" alt="GitHub Link"/></a></div>
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
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  background-color: #f5f5f5;
  padding: 0px 100px;
}
#footerHeader {
  font-family: 'Lobster Two', cursive;
  color: grey;
  font-weight: bold;
  font-size: 36px;
  padding: 38px 0px;
}
#contactList {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  font-size: 18px;
  padding: 30px 0px;
}
.contactTab {
  display: flex;
  align-items: center;
}
.contactImage {
  width: 35px;
  margin: 0px 10px;
}

#emailLink {
  text-decoration: none;
  color: grey;
  padding-bottom: 5px;
}
</style>
