<template lang="html">
   <div class="container">
      <div class="left-part"
           :style="{ backgroundImage: 'url(' + left + ')'}">
           <div class="headbar-menu">
              <nuxt-link to="/">Home</nuxt-link>
              <nuxt-link to="ARCHITECT">Architect</nuxt-link>
              <nuxt-link to="Styles">Styles</nuxt-link>
              <nuxt-link to="Trends">Trends</nuxt-link>
           </div>
    <p>Architecture is both the process and<br>
         the product of planning, designing<br>
          and constructing buildings or any<br>
           other structures. Architectural<br>
            works, in the material form of<br>
             buildings, are often perceived<br>
              as cultural symbols and as<br>
               works of art.  Historical<br>
                civilizations are often<br>
                 identified with their<br>
                 surviving architectural<br>
                        achievements.</p>
      </div>
      <div class="center-photo"
           :style="{ backgroundImage: 'url(' + woman + ')'}">
           <h1>Archart</h1>
           <div id="menu"
           v-bind:style="{ visibility: displaya }">
           </div>
           <div class="menu-links"
           v-bind:style="{ visibility: displaya }">
           <nuxt-link to="/">Home</nuxt-link>
           <nuxt-link to="ARCHITECT">Architect</nuxt-link>
           <nuxt-link to="Styles">Styles</nuxt-link>
           <nuxt-link to="Trends">Trends</nuxt-link>
         </div>
      </div>
       <div class="right-part" id="particles-js">
         <div class="phone-menu" v-on:click="menu">
              <hr>
              <hr>
              <hr>
         </div>

         <div class="main-block">
           <div class="double">
             <div class="arch-block">
               <div class="build-image">&#160;</div>
                 <img v-bind:src="icons[0]" alt="">
               <h4>{{ archis[0] }}</h4>
             </div>
             <div class="arch-block">
               <div class="build-image">&#160;</div>
                 <img v-bind:src="icons[1]" alt="">
               <h4>{{ archis[1] }}</h4>
             </div>
           </div>
           <div class="double">
             <div class="arch-block">
               <div class="build-image">&#160;</div>
               <img :src="arts[0]" v-bind:style="{width: width1}">
               <h4>{{ tects[0] }}</h4>
             </div>
             <div class="arch-block">
               <div  class="build-image">&#160;</div>
                 <img :src="arts[1]"   v-bind:style="{width: width, marginTop: top }" alt="">
               <h4>{{ tects[1] }}</h4>
             </div>
           </div>
         </div>
      </div>
      <script type="text/javascript" src="particles.js"></script>
      <script type="text/javascript" src="app.js"></script>
   </div>
</template>

<script>
export default {
  data() {
    return{
      left: "./headbar/left.jpg",
      woman: "./headbar/woman.jpg",
      right: "./headbar/right.jpg",
      archis: ["Renaissance", "Gothic"],
      tects:  ["High-tech", "Digital"],
      icons: ["headbar/Renaissans.svg", "headbar/2.svg"],
      arts: ["headbar/higttecl.svg", "headbar/digital.svg"],
      width: "92%",
      width1: "39%",
      top: "-64%",
      top1: "-93%",
      left1: "-20%",
      topa: "-110vw",
      displaya: "hidden"
    }
  },
  // mounted:function() {
  //     if(window.screen.width < 480){
  //       this.left1 = "10%";
  //     }
  //   },
    methods: {
       menu: function() {
         if( this.left1 == '-20%' ){
           this.left1 = '0vw';
         }else{
           this.left1 = '-20%';
        }
         if( this.displaya == 'hidden' ){
           this.displaya = 'visible';
         }else{
           this.displaya = 'hidden';
        }
        var menu = document.getElementById("menu");
        if( menu.style.opacity == "1" ){
            menu.style.opacity = "0";
        }else{
          menu.style.opacity = "1";
        }
        var lol = document.getElementsByClassName("menu-links");
        // console.log(lol[0]);
        if( lol[0].style.opacity == "1" ){
            lol[0].style.opacity = "0";
        }else{
          lol[0].style.opacity = "1";
        }
    }
  },
}
</script>

<style lang="sass" scoped>
@import '../assets/variables'
#particles-js
  background: #242222
  z-index: 1
.container
  display: flex
  width: 100%
  height: 47.25vw
  overflow: hidden
@media screen and (max-width: 768px)
  .container
    flex-direction: row-reverse
    height: 50vw
@media screen and (max-width: 480px)
  .container
    height: 100vw
.left-part
  width: 50%
  background-repeat: no-repeat, no-repeat
  background-size: cover
  z-index: 1
  padding-bottom: 15%
@media screen and (max-width: 768px)
  .left-part
    width: 60%
@media screen and (max-width: 480px)
  .left-part
    display: none
.headbar-menu
  display: flex
  justify-content: space-between
  width: 90%
  padding-top: 3.5%
  padding-left: 5vw
@media screen and (max-width: 768px)
  .headbar-menu
    display: none
.headbar-menu a
  color: #232799
  font-family: GRACETIANS
  text-decoration: none
  font-size: 1.2rem
@media screen and (max-width: 1024px)
  .headbar-menu a
    font-size: 1rem
.left-part p
  text-align: right
  font-family: GRACETIANS
  font-size: 1.15vw
  line-height: 1.6
  padding-top: 14%
  padding-right: 30%
@media screen and (max-width: 768px)
  .left-part p
    font-size: 1.8vw
    padding-right: 6%
.center-photo
  display: flex
  justify-content: center
  position: absolute
  left: 0
  right: 0
  margin: 0 auto
  margin-top: 5.35vw
  background-size: cover
  width: 28vw
  height: 41.90vw
  z-index: 2
@media screen and (max-width: 768px)
  .center-photo
     position: relative
     margin-top: 0vw
     width: 40vw
     height: 50vw
@media screen and (max-width: 480px)
  .center-photo
     position: relative
     margin-top: 10vw
     width: 60vw
     height: 90vw
     z-index: 2
     display: flex
.center-photo h1
  font-family: GRACETIANS-Cutting
  color: white
  padding-top: 1vw
  font-size: 5vw
@media screen and (max-width: 480px)
  .center-photo h1
    position: absolute
    padding-top: 2vw
    font-size: 11vw
.right-part
  z-index: 1
  display: flex
  width: 50%
.menu-links
  display: none
@media screen and (max-width: 768px)
  .right-part
    width: 15%
@media screen and (max-width: 480px)
  .right-part
    position: absolute
    width: 100vw
    height: 100vw
    z-index: 0
.right-part img
  width: 100%
.phone-menu
  display: none
@media screen and (max-width: 768px)
  .phone-menu
    position: absolute
    display: flex
    flex-direction: column
    align-items: center
    margin: 0 auto
    width: auto
    margin-top: 30%
@media screen and (max-width: 768px)
  .phone-menu
    position: absolute
    display: flex
    flex-direction: column
    align-items: center
    margin: 0 auto
    width: auto
    margin-top: 3%
  .phone-menu hr
    color: white
    transition: 0.5s
    margin-bottom: 20%
    margin-left: 50%
    width:  50px
@media screen and (max-width: 480px)
  .phone-menu
    position: absolute
    width:  100vw
    padding-left: 5%
    padding-right: 95%
    height: 10vw
    background: black
    margin-top: 0%
    padding-top: 2.4vw
    padding-left: 10%
    opacity: 0.65
    z-index: 4
  .phone-menu hr
    margin-bottom: 2vw
.menu
  display: none
  transition: 1s
@media screen and (max-width: 768px)
  #menu
    position: absolute
    top: 0%
    width: 35vw
    display: flex
    flex-direction: column
    background: -moz-linear-gradient(270deg, rgba(255,255,255,0) 0%, rgba(255,255,255,0.08) 8%, rgba(0,30,128,1) 100%); /* ff3.6+ */
    height: 50vw
    transition: visibility 1.5s, opacity 1.5s
    opacity: 0
    padding-top: 3%
    padding: 1%
  .menu-links
    position: absolute
    display: flex
    margin-right: 28%
    flex-direction: column
    transition: visibility 1.5s, opacity 1.5s
    opacity: 0
  .menu-links a
    color: white
    font-size: 4vw
    text-decoration: none
    margin-bottom: 3vw
    font-family: GRACETIANS
  .menu-links a:nth-child(1)
    padding-top: 20vw
@media screen and (max-width: 480px)
  #menu
    width: 62vw
    height: 100vw
  .menu-links
    margin-right: 30%
  .menu-links a
    font-size: 7vw
    margin-bottom: 3vw
  .menu-links a:nth-child(1)
    padding-top: 45vw
.main-block
  position: absolute
  margin-top: 19vw
  display: flex
  width: 22%
  height: 21vw
  flex-direction: center
  margin-left: 20%
@media screen and (max-width: 768px)
  .main-block
    display: none
.double
  display: flex
  flex-direction: column
  width: 45%
  height: 100%
  margin: 1%
.arch-block
  position: relative
  top: 0
  display: flex
  flex-direction: column
  align-items: center
  text-align: center
  width: 100%
  height: 50%
  // background: #181a66
  margin: 0 auto
  transition: 0.4s
  // opacity: 0.85
.arch-block:hover
 top: -4px
.build-image
  background: #181a66
  padding-bottom: 84%
  z-index: 1
  opacity: 0.6
  width: 100%
.arch-block img
  margin-top: -95%
  width: 55%
  z-index: 2
.arch-block h4
  font-family: GRACETIANS
  font-size: 1.2vw
  font-weight: 100
  z-index: 2
  color: white
</style>
