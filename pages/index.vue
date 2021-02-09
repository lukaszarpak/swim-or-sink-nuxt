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
  },
  head: {
    title: 'Swim or Sink',
    titleTemplate: 'Swim or Sink',
    htmlAttrs: {
      lang: 'pl',
      amp: true
    },
    meta: [
      { charset: 'utf-8' },
      {
        name: 'viewport',
        content: 'width=device-width, initial-scale=1'
      },
      {
        hid: 'description',
        name: 'description',
        content:
          'The amazing Nuxt application that teaches me all the cool features of Nuxt'
      }
    ],
    link: [
      {

      }
    ],
    script: [
      {
        src: 'https://kit.fontawesome.com/921fcf519c.js',
        crossorigin: 'anonymous'
      }
    ]
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
