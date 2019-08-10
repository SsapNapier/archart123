<template lang="html">
  <div class="container">
    <div class="first-block">
    <div class="text">
      <h1>Renaissance</h1>
      <p>Renaissance architecture is the European architecture of the period between the early 14th and early 16th centuries in different regions, demonstrating a conscious revival and development of certain elements of ancient Greek and Roman thought and material culture.<br><br> Stylistically, Renaissance architecture followed Gothic architecture and was succeeded by Baroque architecture. Developed first in Florence, with Filippo Brunelleschi as one of its innovators, the Renaissance style quickly spread to other Italian cities. The style was carried to France, Germany, England, Russia and other parts of Europe at different dates and with varying degrees of impact. </p>
      </div>
      <div class="photo">
         <img src="/slider/1.jpg" alt="">
      </div>
    </div>
    <div class="second-block">
      <div class="photo"
        v-bind:style="{ width: width1 }">
        <img src="/slider/2.jpg"
        v-bind:style="{ width: width }"
         alt="">
      </div>
      <div class="text">
        <h1>Gothic</h1>
        <p>Gothic architecture (Latin: francigenum opus) is a style that flourished in Europe during the High and Late Middle Ages. It evolved from Romanesque architecture and was succeeded by Renaissance architecture. Originating in 12th-century France, it was widely used, especially for cathedrals and churches, until the 16th century.
<br><br>
Its most prominent features included the use of the rib vault and the flying buttress, which allowed the weight of the roof to be counterbalanced by buttresses outside the building, giving greater height and more space for windows. Another important feature was the extensive use of stained glass, and the rose window, to bring light and color to the interior.<br><br> Another feature was the use of realistic statuary on the exterior, particularly over the portals, to illustrate biblical stories for the largely illiterate parishioners. Some key architectural features, such as the pointed arch and the rib vault, were adopted from outside Europe, probably deriving from Islamic architecture. These features had both existed in Romanesque architecture, but they were used more extensively and in more innovative ways to make Gothic cathedrals higher, stronger, and filled with light.
</p>
  </div>
    </div>
    <div class="third-block">
    <div class="text">
      <h1>High-tech</h1>
      <p>High-tech architecture, also known as Structural Expressionism, is a type of Late Modern architectural style that emerged in the 1970s, incorporating elements of high-tech industry and technology into building design. High-tech architecture appeared as revamped modernism, an extension of those previous ideas helped by even more technological advances.<br><br> This category serves as a bridge between modernism and post-modernism; however, there remain grey areas as to where one category ends and the other begins. In the 1980s, high-tech architecture became more difficult to distinguish from post-modern architecture. Some of its themes and ideas were later absorbed into the style of Neo-Futurism art and architectural movement.  </p>
      </div>
      <div class="photo">
         <img src="/slider/3.jpg" alt="">
      </div>
    </div>
    <div class="fourth-block">
      <div class="photo"
        v-bind:style="{ width: width1 }">
        <img src="/slider/4.jpg"
        v-bind:style="{ width: width }"
         alt="">
      </div>
      <div class="text">
        <h1>Digitale</h1>
        <p>Digital architecture has been used to refer to other aspects of architecture that feature digital technologies. The emergent field is not clearly delineated to this point, and the terminology is also used to apply to digital skins that can be streamed images and have their appearance altered.<br><br> A headquarters building design for Boston television and radio station WGBH by Polshek Partnership has been discussed as an example of digital architecture and includes a digital skin.</p>
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
.third-block,
.fourth-block
  display: flex
  width: 82%
  margin: 0 auto
  padding-top: 2%
  justify-content: space-between
.fourth-block
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
