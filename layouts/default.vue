<template>
  <div>
    <Controls id="home" />
    <Nuxt />
    <FooterComponent />
  </div>
</template>

<script>
import Controls from '../components/Navbar/Controls.vue'
import FooterComponent from '../components/Footer/Footer.vue'

export default {
  name: 'App',
  components: {
    Controls,
    FooterComponent
  }
}
</script>
