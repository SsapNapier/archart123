<template>
  <div class="Container">
    <div class="Acrh">
     <div class="left-part">
        <h2>About the architecture</h2>
        <p>The earliest surviving written work on the subject of architecture is De architectura,
           by the Roman architect Vitruvius in the early 1st century AD. According to Vitruvius,
           a good building should satisfy the three principles of firmitas, utilitas, venustas,
           commonly known by the original translation – firmness, commodity and delight.
           An equivalent in modern English would be:
           <br><br>
           	&#8226; Durability – a building should stand up robustly and remain in good condition.<br>
           	&#8226; Utility – it should be suitable for the purposes for which it is used.<br>
           	&#8226; Beauty – it should be aesthetically pleasing.</p>
                    <nuxt-link to="ARCHITECT">
                      <button type="button" name="button">Read more</button>
                    </nuxt-link>
     </div>
     <div class="right-part">
        <img src="Content/1.png" alt="">
     </div>
   </div>
   <div class="slider">
     <div class="buttons">
         <button type="button" class="tom" @click="changeSlide" id="color" v-bind:style="{ color: red }" name="0">{{ this.names[0] }}</button>
         <button type="button" class="tom" @click="changeSlide" id="color" name="1">{{ this.names[1] }}</button>
         <button type="button" class="tom" @click="changeSlide" id="color" name="2">{{ this.names[2] }}</button>
         <button type="button" class="tom" @click="changeSlide" id="color" name="3">{{ this.names[3] }}</button>
     </div>
     <div class="info-block">
       <div class="photo-block">
          <img :src="this.images[i]" alt="">
       </div>
       <div class="text-block">
           <h2>{{ this.names[i] }}</h2>
           <p>{{ this.textes[i] }}</p>
           <nuxt-link to="styles">
             <button type="button" name="button">Read more</button>
           </nuxt-link>
       </div>
     </div>
   </div>
   <div class="trends">
     <div class="text-left">
        <h2>Trends in architecture</h2>
        <p>Since the 1980s, as the complexity of buildings began to increase (in terms of structural systems, services, energy and technologies), the field of architecture became multi-disciplinary with specializations for each project type, technological expertise or project delivery methods.<br>
          <br>
           In addition, there has been an increased separation of the 'design' architect from the 'project' architect who ensures that the project meets the required standards and deals with matters of liability.</p>
           <nuxt-link to="Trends">
             <button type="button" name="button">Read more</button>
           </nuxt-link>
     </div>
     <div class="photo-right">
        <img src="Content/2.png" alt="">
     </div>
   </div>
  </div>
</template>

<script>
export default {
  data() {
    return{
      i: 0,
      red: "#007eff",
      images: ["slider/1.jpg", "slider/2.jpg", "slider/3.jpg", "slider/4.jpg"],
      names: ["Renaissance", "Gothic", "High-tech", "Modern"],
      textes: ["In Renaissance Europe, from about 1400 onwards, there was a revival of Classical learning accompanied by the development of Renaissance Humanism which placed greater emphasis on the role of the individual in society than had been the case during the Medieval period. Buildings were ascribed to specific architects – Brunelleschi, Alberti, Michelangelo, Palladio – and the cult of the individual had begun. There was still no dividing line between artist, architect and engineer, or any of the related vocations, and the appellation was often one of regional preference.", "Gothic architecture is a style that flourished in Europe during the High and Late Middle Ages. It evolved from Romanesque architecture and was succeeded by Renaissance architecture. Originating in 12th-century France, it was widely used, especially for cathedrals and churches, until the 16th century.", "High-tech architecture, also known as Structural Expressionism, is a type of Late Moder architectural style that emerged in the 1970s, incorporating elements of high-tech industry and technology into building design. High-tech architecture appeared as revamped modernism, an extension of those previous ideas helped by even more technological advances. This category serves as a bridge between modernism and post-modernism.",  "Modern architecture, or modernist architecture was based upon new and innovative technologies of construction, particularly the use of glass, steel and reinforced concrete; the idea that form should follow function; an embrace of minimalism; and a rejection of ornament."]
    }
  },
  methods: {
    changeSlide(event){
      this.i = event.target.name;
      var aik = document.getElementsByClassName("tom");
      aik[0].style.color = "white";
      aik[1].style.color = "white";
      aik[2].style.color = "white";
      aik[3].style.color = "white";
      event.target.style.color = "#007eff";
    }
  }
}
</script>

<style lang="sass" scoped>
@import '../assets/variables'
.Container
  font-family: JervinhoRegular
  background: #e6e6e6
.Acrh
  display: flex
  padding-top: 3%
  padding-bottom: 3%
  width: 84%
  margin: 0 auto
.left-part
  display: flex
  flex-direction: column
  justify-content: center
  width: 50%
  align-items: left
.left-part h2
  padding-bottom: 5%
.left-part h2,
.left-part p
  width: 80%
.left-part a
  margin-top: 4%
  width: 20%
  height: 25px
.left-part button
  border: 1px solid black
  background: none
  width: 100%
  height: 25px
.left-part button:hover
  background: #363999
  color: white
.right-part
  display: flex
  flex-direction: center
  width: 50%
.right-part img
  width: 100%
// SLIDER
.slider
  display: flex
  flex-direction: column
  width: 100%
  margin: 0 auto
  background: #333030
  color: white
.buttons
  display: flex
  width: 86%
  margin: 0 auto
.buttons button
  border: 2px solid white
  margin: 1%
  width: (96% / 4)
  height: 30px
  font-size: 0.83rem
  background: #1a1818
  color: white
.info-block
  display: flex
  justify-content: space-between
  width: 84%
  margin: 0 auto
  padding-top: 1%
  padding-bottom: 2%
.photo-block
  display: flex
  width: 45%
.photo-block img
  width: 100%
.text-block
  display: flex
  flex-direction: column
  justify-content: center
  width: 48%
.text-block h2
  padding-bottom: 8%
@media screen and (max-width: 768px)
  .info-block
    align-items: center
    flex-direction: column-reverse
  .photo-block
    width: 80%
  .text-block
    width: 100%
    align-items: center
  .text-block h2
    padding-bottom: 4%
    text-align: center
.text-block p
  padding-bottom: 8%
.text-block a
  width: 20%
.text-block button
  border: 1px solid white
  color: white
  background: none
  width: 100%
  height: 25px
@media screen and (max-width: 768px)
  .text-block p
    padding-bottom: 3%
  .text-block button
    margin-bottom: 10%
.text-block button:hover
  background: #363999
  color: white
.trends
  display: flex
  margin: 0 auto
  padding-top: 2%
  padding-bottom: 1.7%
  justify-content: space-between
  width: 84%
.text-left
  display: flex
  flex-direction: column
  justify-content: center
  width: 40%
.text-left  h2
  padding-bottom: 5%
.text-left a
  margin-top: 4%
  width: 24%
.text-left button
  border: 1px solid black
  background: none
  width: 100%
  height: 25px
.text-left button:hover
  background: #363999
  color: white
.photo-right
  width: 48%
.photo-right img
  width: 100%
</style>
