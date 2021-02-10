<template>
  <div id="app">
    <Landing />
    <Boxes />
    <About id="section0" />
    <Trainers id="section2" />
    <Reviews />
  </div>
</template>

<script>
import Landing from '../components/LandingPage/Landing.vue'
import Boxes from '../components/BoxSection/Boxes.vue'
import About from '../components/AboutUs/About.vue'
import Trainers from '../components/TrainersSection/Trainers.vue'
import Reviews from '../components/CustomerReviews/Reviews.vue'

export default {
  name: 'App',
  components: {
    Landing,
    Boxes,
    About,
    Trainers,
    Reviews
  }
}
</script>

<style lang="scss">
#app {
  overflow-x: hidden;
}
html {
  scroll-behavior: smooth;
}

.close,
.prev,
.next {
  /* styling photo gallery */
  color: white !important;
}
</style>
