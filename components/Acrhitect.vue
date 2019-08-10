<template lang="html">
  <div class="container">
    <div class="first-block">
    <div class="text">
      <h1>Definitions and etymology</h1>
      <h2>Architecture can mean:</h2>
      <p> - A general term to describe buildings and other physical structures.<br>
      - The art and science of designing buildings and (some) nonbuilding structures.<br>
      - The style of design and method of construction of buildings and other physical structures.<br>
      - A unifying or coherent form or structure.<br>
      - Knowledge of art, science, technology, and humanity.<br>
      - The design activity of the architect, from the macro-level (urban design, landscape architecture) to the micro-level (construction details and furniture).<br>
      - The practice of the architect, where architecture means offering or rendering professional services in connection with the design and construction of buildings,
      or built environments.</p>
      </div>
      <div class="photo">
         <img src="/architect/tobias-keller-2ecH5Lw3zSk-unsplash.jpg" alt="">
      </div>
    </div>
    <div class="second-block">
      <div class="photo"
        v-bind:style="{ width: width1 }">
        <img src="/architect/joel-filipe-RFDP7_80v5A-unsplash.jpg"
        v-bind:style="{ width: width }"
         alt="">
      </div>
      <div class="text">
        <h1>Historic treatises</h1>
        <p>The earliest surviving written work on the subject of architecture is De architectura,
          by the Roman architect Vitruvius in the early 1st century AD. According to Vitruvius,
          a good building should satisfy the three principles of firmitas, utilitas, venustas,
          commonly known by the original translation – firmness, commodity and delight. An equivalent in modern English would be:<br><br>
          - Durability – a building should stand up robustly and remain in good condition.<br>
          - Utility – it should be suitable for the purposes for which it is used.<br>
          - Beauty – it should be aesthetically pleasing.<br><br>
          According to Vitruvius, the architect should strive to fulfill each of these three
          attributes as well as possible. Leon Battista Alberti, who elaborates on the ideas
          of Vitruvius in his treatise, De Re Aedificatoria, saw beauty primarily as a matter
          of proportion, although ornament also played a part. For Alberti, the rules of proportion
          were those that governed the idealised human figure, the Golden mean.<br><br>
          <p>The most important aspect of beauty was, therefore, an inherent part of an object,
             rather than something applied superficially, and was based on universal,
             recognisable truths. The notion of style in the arts was not developed until
             the 16th century, with the writing of Vasari: by the 18th century, his Lives
             of the Most Excellent Painters, Sculptors, and Architects had been translated into Italian, French, Spanish, and English.</p>
      </div>
    </div>
    <div class="third-block">
    <div class="text">
      <h1>Modern concepts</h1>
      <p>The notable 19th-century architect of skyscrapers, Louis Sullivan, promoted an overriding precept to architectural design: "Form follows function".
While the notion that structural and aesthetic considerations should be entirely
 subject to functionality was met with both popularity and skepticism, it had<br><br>
the effect of introducing the concept of "function" in place of Vitruvius' "utility".
"Function" came to be seen as encompassing all criteria of the use, perception and
enjoyment of a building, not only practical but also aesthetic, psychological and cultural.<br><br>
Nunzia Rondanini stated, "Through its aesthetic dimension architecture goes beyond the functional aspects that it has in common with other human sciences. Through its own particular way of expressing values, architecture can stimulate and influence social life without presuming that, in and of itself, it will promote social development.'
<br><br>
To restrict the meaning of (architectural) formalism to art for art's sake is not only reactionary; it can also be a purposeless quest for perfection or originality which degrades form into a mere instrumentality".

Among the philosophies that have influenced modern architects and their approach to building design are Rationalism, Empiricism, Structuralism, Poststructuralism, Deconstruction and phenomenology. </p>
      </div>
      <div class="photo">
         <img src="/architect/joel-filipe-jU9VAZDGMzs-unsplash.jpg" alt="">
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
