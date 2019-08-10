<template>
  <div class="container">
      <headbar />
      <Acrhitect />
      <Footer />
  </div>
</template>

<script>
import headbar from '~/components/headbar.vue'
import Acrhitect from '~/components/Acrhitect.vue'
import Content from '~/components/Content.vue'
import Footer from '~/components/Footer.vue'
// import Builds from '~/components/Builds.vue'

export default {
  components: {
    headbar,
    Acrhitect,
    Footer
  }
}
</script>

<style>

</style>
