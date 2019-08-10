<template>
  <div class="footer"
       :style="{ backgroundImage:  'url(' + Image + ')'}">
  <div class="container">
    <div class="double">
      <div class="about-us">
        <h2>Web-app<br> about architect</h2>
        <p>This page was made for<br>
          to introduce to others<br>
          my skills in web-developing<br>
          and design</p>
        </div>
        <div class="navigation">
          <h2>links</h2>
          <a href="#">Home</a>
          <a href="#">Architect</a>
          <a href="#">Styles</a>
          <a href="#">Trends</a>
        </div>
    </div>
    <div class="double">
      <div class="styles">
        <h2>Styles</h2>
        <a href="#">Renaissance</a>
        <a href="#">Gothic</a>
        <a href="#">High-tech</a>
        <a href="#">Modern</a>
      </div>
      <div class="contacts">
        <h2>Our contacts</h2>
        <p>+2 392 3929 210</p>
        <p>info@yourdomain.com</p>
        <p>203 Fake St. Mountain View,<br> San Francisco, California,<br> USA</p>
      </div>
    </div>
   </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      Image: "https://raw.githubusercontent.com/Arch-art/Arch-art.github.io/master/3.jpg"
    }
  }
}
</script>

<style lang="sass" scoped>
@import '../assets/variables'
.footer
  background-size: cover
  font-family: GRACETIANS
  font-size: 0.83rem
.container
  display: flex
  justify-content: space-between
  width: 82%
  margin: 0 auto
  padding-top: 4%
  padding-bottom: 3%
  color: white
.double
  display: flex
  justify-content: space-between
  width: 43%
@media screen and (max-width: 1024px)
  .container
    width: 95%
  .double
    width: 47%
@media screen and (max-width: 768px)
  .container
    flex-direction: column
    width: 85%
  .double
    width: 400px
  .double:nth-child(2)
    flex-direction: row-reverse
    width: 420px
    padding-top: 4%
  .double div
    flex-shrink: 0
@media screen and (max-width: 480px)
  .container
    width: 65%
  .double,
  .double:nth-child(2)
    flex-direction: column
    width: auto
.container a
  color: white
  text-decoration: none
.about-us p
  font-weight: 100
  margin-top: 8%
  line-height: 1.6
.navigation
  display: flex
  flex-direction: column
.navigation h2
  margin-bottom: 20%
.styles h2
  margin-bottom: 16%
@media screen and (max-width: 480px)
  .about-us p
    margin-top: 2%
  .navigation h2
    margin-top: 4%
    margin-bottom: 0%
  .styles h2
    margin-top: 2%
    margin-bottom: 0%
.contacts h2
  margin-bottom: 7%
.navigation a
  margin-top: 18%
@media screen and (max-width: 480px)
  .contacts h2
    margin-top: 4%
    margin-bottom: 0%
  .navigation a
    margin-top: 2%
    width: 4%
.styles
  display: flex
  flex-direction: column
.styles a
  margin-top: 15%
@media screen and (max-width: 480px)
  .styles a
    margin-top: 2%
    width: 20%
.contacts
  display: flex
  flex-direction: column
.contacts p
  margin-top: 7%
@media screen and (max-width: 480px)
  .contacts p
    margin-top: 2%
</style>
