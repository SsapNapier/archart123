<template>
  <div class="container">
      <headbar />
      <trends />
      <Footer />
      <!-- <Builds /> -->
  </div>
</template>

<script>
import headbar from '~/components/headbar.vue'
import trends from '~/components/trends.vue'
import Footer from '~/components/Footer.vue'
// import Builds from '~/components/Builds.vue'

export default {
  components: {
    headbar,
    trends,
    Footer
  }
}
</script>

<style>

</style>
