<template lang="html">
  <div class="container">
    <div class="first-block">
    <div class="text">
      <h1>Architecture today</h1>
      <p>Since the 1980s, as the complexity of buildings began to increase (in terms of structural systems, services, energy and technologies), the field of architecture became multi-disciplinary with specializations for each project type, technological expertise or project delivery methods. In addition, there has been an increased separation of the 'design' architect [Notes 1] from the 'project' architect who ensures that the project meets the required standards and deals with matters of liability.</p>
    </div>
      <div class="photo">
         <img src="/trends/1.jpg" alt="">
      </div>
    </div>
    <div class="second-block">
      <div class="photo"
        v-bind:style="{ width: width1 }">
        <img src="/trends/2.jpg"
        v-bind:style="{ width: width }"
         alt="">
      </div>
      <div class="text">
        <h1>SSSSSSSSS</h1>
        <p>The preparatory processes for the design of any large building have become increasingly complicated, and require preliminary studies of such matters as durability, sustainability, quality, money, and compliance with local laws.
<br><br>
 A large structure can no longer be the design of one person but must be the work of many. Modernism and Postmodernism have been criticised by some members of the architectural profession who feel that successful architecture is not a personal, philosophical, or aesthetic pursuit by individualists; rather it has to consider everyday needs of people and use technology to create liveable environments, with the design process being informed by studies of behavioral, environmental, and social sciences.
</p>
  </div>
    </div>
    <div class="third-block">
    <div class="text">
      <h1>High-tech</h1>
      <p>Environmental sustainability has become a mainstream issue, with profound effect on the architectural profession. Many developers, those who support the financing of buildings, have become educated to encourage the facilitation of environmentally sustainable design, rather than solutions based primarily on immediate cost. <br><br> Major examples of this can be found in passive solar building design, greener roof designs, biodegradable materials, and more attention to a structure's energy usage. This major shift in architecture has also changed architecture schools to focus more on the environment. There has been an acceleration in the number of buildings which seek to meet green building sustainable design principles.  </p>
      </div>
      <div class="photo">
         <img src="/trends/3.jpg" alt="">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      width: "100%",
      width1: "40%"
    }
  }
}
</script>

<style lang="sass" scoped>
@import '../assets/variables'
.container
  font-family: JervinhoRegular
  background: #e6e6e6
.first-block,
.second-block,
.third-block
  display: flex
  width: 82%
  margin: 0 auto
  padding-top: 2%
  justify-content: space-between
.third-block
  padding-bottom: 2%
.text
  display: flex
  flex-direction: column
  justify-content: center
  width: 45%
.text h1
  padding-bottom: 2%
.text h2
  padding-bottom: 2%
.photo
  display: flex
  justify-content: center
  width: 50%
.photo img
  width: 100%
</style>
