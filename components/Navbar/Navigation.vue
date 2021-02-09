<template>
  <div class="mobile">
    <div class="container">
      <div class="row">
        <div class="col-12 col-md-2 mx-auto">
          <a @click="isActive0 = true">Galeria</a>
        </div>
        <div class="col-12 col-md-2 mx-auto">
          <a @click="isActive1 = true">Grafik</a>
        </div>
        <div class="col-12 col-md-2 mx-auto">
          <a @click="isActive2 = true">Cennik</a>
        </div>
        <div
          v-for="(item, index) in menu"
          :key="index"
          class="col-12 col-md-2 mx-auto"
          @click="hideMenu"
        >
          <a :href="`#section${index}`">{{ item }}</a>
        </div>
      </div>
    </div>
    <transition name="fade" type="transition">
      <Sheets v-if="isActive1" @sheetDel="update">
        <h2 slot="title">
          Grafik Zajęć
        </h2>
        <h3 slot="day1">
          Sobota
        </h3>
        <div slot="description1">
          <p>18:00 grupa podstawowa – mały basen</p>
          <p>18:30 grupa podstawowa – duży basen</p>
          <p>19:00 grupa średnio zaawansowana – duży basen</p>
          <p>19:30 grupa zaawansowana – duży basen</p>
        </div>
        <h3 slot="day2">
          Niedziela
        </h3>
        <div slot="description2">
          <p>18:00 grupa podstawowa – mały basen</p>
          <p>18:30 grupa podstawowa – duży basen</p>
          <p>19:00 grupa średnio zaawansowana – duży basen</p>
          <p>19:30 grupa zaawansowana – duży basen</p>
        </div>
        <h3 slot="day3">
          Poniedziałek
        </h3>
        <div slot="description3">
          <p>18:30 grupa podstawowa i średnio zaawansowana – duży basen</p>
          <p>19:00 grupa średnio zaawansowana i zaawansowana – duży basen</p>
        </div>
      </Sheets>
    </transition>
    <transition name="fade">
      <Sheets v-if="isActive2" @sheetDel="update">
        <h2 slot="title">
          Cennik
        </h2>
        <h3 slot="day1">
          Zajęcia grupowe
        </h3>
        <div slot="description1">
          <p>(15 lekcji) – 600zł płatne w dwóch równych ratach</p>
          <p style="margin-top: 15px">
            *Cena zawiera wejście uczestnika na basen.
          </p>
        </div>
        <h3 slot="day2">
          Lekcje indywidualne
        </h3>
        <div slot="description2">
          <p>1os. - 50zł</p>
          <p>2os. - 80zł</p>
          <p>3os. - 100zł</p>
          <p style="margin-top: 15px">
            *Wejście na basen płatne we własnym zakresie.
          </p>
        </div>
        <h3 slot="day3" />
        <div slot="description3">
          <p>Czas trwania lekcji – 30min</p>
          <p>Miejsce zajęć – Basen GOSiR w Piasecznie, ul. Sikorskiego 20.</p>
        </div>
      </Sheets>
    </transition>
    <transition name="fade">
      <Gallery v-if="isActive0" @sheetDel="update" />
    </transition>
  </div>
</template>
<script>
import Sheets from '../BoxSection/Sheets'
import Gallery from '../BoxSection/Gallery.vue'
export default {
  components: {
    Sheets,
    Gallery
  },
  props: {
    activate: Boolean
  },
  data: () => ({
    isActive0: false,
    isActive1: false,
    isActive2: false,
    menu: ['O nas', 'Kontakt']
  }),
  methods: {
    hideMenu () {
      this.$emit('hideMenu')
    },
    update (active) {
      this.isActive0 = active
      this.isActive1 = active
      this.isActive2 = active
    }
  }
}
</script>
<style lang="scss" scoped>
.mobile {
  position: fixed;
  top: 100px;
  left: 0;
  width: 100%;
  z-index: 3;
  transition: 0.3s;
  .container {
    margin: 0 auto;
    .row {
      margin: 0;
      padding: 0;
      background-color: #fff;
      border-bottom-left-radius: 30px;
      border-bottom-right-radius: 30px;
      border: solid 2px #0b70b8;
      div {
        list-style: none;
        font-size: 20px;
        width: 120px;
        text-align: center;
        a {
          color: #2d3681;
          display: block;
          line-height: 90px;
          cursor: pointer;
        }
        a:hover {
          text-decoration: none;
          font-weight: 700;
        }
      }
    }
  }
}
.slide-enter {
  transform: translateY(-100%);
}
.slide-enter-active {
  transition: transform 0.2s;
}
/* .slide-leave {

} */
.slide-leave-active {
  transition: transform 0.2s;
  transform: translateY(-100%);
}
</style>
