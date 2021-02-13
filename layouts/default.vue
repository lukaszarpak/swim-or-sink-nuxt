<template>
  <div>
    <Controls id="home" />
    <Nuxt />
    <Contact id="section1" />
    <FooterComponent />
    <!-- <CookieLaw button-text="Zgadzam się" button-decline="true" button-decline-text="Nie zgadzam się">
      <div slot="message">
        W ramach naszej witryny stosujemy pliki cookies w celu świadczenia Państwu usług na najwyższym poziomie,
        w tym w sposób dostosowany do indywidualnych potrzeb. Więcej szczegółów w
        <Nuxt-link to="/dokumenty/cookies">
          Polityce Cookies
        </Nuxt-link>
      </div>
    </CookieLaw> -->
  </div>
</template>

<script>
// import CookieLaw from 'vue-cookie-law'
import Controls from '../components/Navbar/Controls.vue'
import Contact from '../components/ContactSection/Contact.vue'
import FooterComponent from '../components/Footer/Footer.vue'

export default {
  name: 'App',
  components: {
    Controls,
    Contact,
    FooterComponent
    // CookieLaw
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
.Cookie {
  .Cookie__buttons {

    button {
      width: 200px;
      text-align: center;
      padding: 1rem;
      border-radius: 30px;
      transition: 0.25s;
      margin: 0.5rem;
    }

    @media (max-width: 767px) {
        width: 100%;

        button {
          width: 100%;
        }
    }

    .Cookie__button {
      background-color: #2fc0df;

      &:hover {
        background-color: #102c4f;
      }
    }

    .Cookie__button--decline {
      white-space: nowrap;
      color: #fff;
      background-color: rgb(182, 182, 182);
    }
  }

}
</style>
