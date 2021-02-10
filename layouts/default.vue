<template>
  <div>
    <Controls id="home" />
    <Nuxt />
    <Contact id="section1" />
    <FooterComponent />
  </div>
</template>

<script>
import Controls from '../components/Navbar/Controls.vue'
import Contact from '../components/ContactSection/Contact.vue'
import FooterComponent from '../components/Footer/Footer.vue'

export default {
  name: 'App',
  components: {
    Controls,
    Contact,
    FooterComponent
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
