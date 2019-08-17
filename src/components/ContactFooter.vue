<template>
  <div id="footer">
    <div id="contactList">
      <div id="email">Email: rssrwn@gmail.com</div>
      <div id="github">Github: rssrwn</div>
      <div id="linkedin">LinkedIn: Ross Irwin</div>
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
  border-top: 1px lightgrey solid;
  height: 60px;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}
#contactList {
  width: 100%;
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  margin: 0px 200px;
  font-size: 18px;
}
</style>
