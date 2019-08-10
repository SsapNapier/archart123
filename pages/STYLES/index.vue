<template>
  <div class="container">
      <headbar />
      <styles />
      <Footer />
      <!-- <Builds /> -->
  </div>
</template>

<script>
import headbar from '~/components/headbar.vue'
import styles from '~/components/styles.vue'
import Footer from '~/components/Footer.vue'
// import Builds from '~/components/Builds.vue'

export default {
  components: {
    headbar,
    styles,
    Footer
  }
}
</script>

<style>

</style>
