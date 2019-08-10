<template>
  <div class="container">
      <headbar />
      <Content />
      <Footer />
      <!-- <Builds /> -->
  </div>
</template>

<script>
import headbar from '~/components/headbar.vue'
import Content from '~/components/Content.vue'
import Footer from '~/components/Footer.vue'
// import Builds from '~/components/Builds.vue'

export default {
  components: {
    headbar,
    Content,
    Footer
  }
}
</script>

<style>

</style>
