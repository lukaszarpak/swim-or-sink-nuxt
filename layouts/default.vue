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
  }
}
</script>
