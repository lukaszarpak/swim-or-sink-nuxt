<template>
  <div>
    <div></div>
    <div></div>
    <div></div>
    <div class="wrap">
      <div class="container">
        <div class="row">
          <div class="col-10 col-md-6 box mx-auto">
            <div class="description">
              <p>Zobacz zdjęcia z zajęć</p>
              <button @click="isActive0=true">Galeria</button>
            </div>
          </div>
          <div class="col-10 col-md-6 box mx-auto">
            <div class="container">
              <div class="row">
                <div class="col-6 boxIn"></div>
                <div class="col-6 boxIn">
                  <div class="description">
                    <p>Grafik zajęć</p>
                    <button @click="isActive1 = true">Grafik</button>

                    <transition name="fade" type="transition">
                      <Sheets v-if="isActive1" @sheetDel="update">
                        <h2 slot="title">Grafik Zajęć</h2>
                        <h3 slot="day1">Sobota</h3>
                        <div slot="description1">
                          <p>18:00 grupa podstawowa – mały basen</p>
                          <p>18:30 grupa podstawowa – duży basen</p>
                          <p>19:00 grupa średnio zaawansowana – duży basen</p>
                          <p>19:30 grupa zaawansowana – duży basen</p>
                        </div>
                        <h3 slot="day2">Niedziela</h3>
                        <div slot="description2">
                          <p>18:00 grupa podstawowa – mały basen</p>
                          <p>18:30 grupa podstawowa – duży basen</p>
                          <p>19:00 grupa średnio zaawansowana – duży basen</p>
                          <p>19:30 grupa zaawansowana – duży basen</p>
                        </div>
                        <h3 slot="day3">Poniedziałek</h3>
                        <div slot="description3">
                          <p>18:30 grupa podstawowa i średnio zaawansowana – duży basen</p>
                          <p>19:00 grupa średnio zaawansowana i zaawansowana – duży basen</p>
                        </div>
                      </Sheets>
                    </transition>
                  </div>
                </div>
                <div class="col-6 boxIn">
                  <div class="description">
                    <p>Przeczytaj więcej o nas</p>
                    <a href="#section0" class="aButton">Poznaj nas</a>
                  </div>
                </div>
                <div class="col-6 boxIn"></div>
              </div>
            </div>
          </div>
          <div class="col-10 col-md-6 box mx-auto">
            <div class="description">
              <p>
                Zobacz ceny
                klikając poniżej
              </p>
              <button @click="isActive2 = true">Cennik</button>

              <transition name="fade">
                <Sheets v-if="isActive2" @sheetDel="update">
                  <h2 slot="title">Cennik</h2>
                  <h3 slot="day1">Zajęcia grupowe</h3>
                  <div slot="description1">
                    <p>(15 lekcji) – 600zł płatne w dwóch równych ratach</p>
                    <p style="margin-top: 15px">*Cena zawiera wejście uczestnika na basen.</p>
                  </div>
                  <h3 slot="day2">Lekcje indywidualne</h3>
                  <div slot="description2">
                    <p>1os. - 50zł</p>
                    <p>2os. - 80zł</p>
                    <p>3os. - 100zł</p>
                    <p style="margin-top: 15px">*Wejście na basen płatne we własnym zakresie.</p>
                  </div>
                  <h3 slot="day3"></h3>
                  <div slot="description3">
                    <p>Czas trwania lekcji – 30min</p>
                    <p>Miejsce zajęć – Basen GOSiR w Piasecznie, ul. Sikorskiego 20.</p>
                  </div>
                </Sheets>
              </transition>
            </div>
          </div>
          <div class="col-10 col-md-6 box mx-auto">
            <div class="description">
              <p>Poznaj naszych trenerów</p>
              <a href="#section2" class="aButton">Trenerzy</a>
            </div>
          </div>
        </div>
      </div>

      <transition name="fade">
        <Gallery v-if="isActive0" @sheetDel="update" />
      </transition>
    </div>
  </div>
</template>
<script>
import Sheets from './Sheets.vue'
import Gallery from './Gallery.vue'
export default {
  data: () => ({
    isActive0: false,
    isActive1: false,
    isActive2: false
  }),
  methods: {
    update (active) {
      this.isActive0 = active
      this.isActive1 = active
      this.isActive2 = active
    }
  },
  components: {
    Sheets,
    Gallery
  }
}
</script>
<style lang="scss" scoped>
.wrap {
  padding: 150px 0 150px 0;
  background-color: #102c4f;
}

.box {
  height: 400px;
  background-color: #ff0066;
  .description {
    color: #fff;
    width: 100%;
    text-align: center;
    margin-top: 160px;
    height: 100px;
  }
}

.box:first-of-type {
  background-image: url("../../assets/swimmingBoy.png");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50% 50%;
}

.box:nth-of-type(4) {
  background-image: url("../../assets/trener1.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50% 50%;
}

.container {
  .container {
    width: 100%;
    padding: 0;
    margin: 0;
  }
}

.boxIn {
  height: 200px;
  margin: 0;
  padding: 0;
  .description {
    color: #fff;
    width: 100%;
    text-align: center;
    margin-top: 60px;
    height: 100px;
  }
}
.boxIn:first-of-type {
  background-image: url("../../assets/swimmingGirl.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50% 50%;
}

.boxIn:nth-of-type(4) {
  background-image: url("../../assets/swimmingClasses.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: 50% 50%;
}

.aButton,
button {
  color: #fff;
  text-decoration: none;
  background: none;
  border: 2px solid #fff;
  border-radius: 30px;
  padding: 10px 20px;
  width: 140px;
  font-weight: 700;
  transition: 0.2s;
  &:hover {
    background: #fff;
    color: #ff0066;
  }
  &:focus {
    outline: none;
  }
}

.aButton {
  display: block;
  margin: auto;
}
</style>
