<template>
  <div class="wrapper">
    <div class="wrap">
      <!-- <Gallery class="gallery" :images="images" :index="index" @close="index = null"></Gallery> -->
      <div class="exit" @click="exitSheet">
        <i class="fas fa-times" />
      </div>
      <div class="d-flex flex-wrap justify-content-center container max-height">
        <div
          v-for="(image, imageIndex) in images"
          :key="imageIndex"
          class="image"
          :style="{ backgroundImage: `url(${image})`}"
          @click="index = imageIndex"
        />
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data: () => ({
    images: [
      require('../../assets/gallery/photo1.jpg'),
      require('../../assets/gallery/photo2.jpg'),
      require('../../assets/gallery/photo3.jpg'),
      require('../../assets/gallery/photo4.jpg'),
      require('../../assets/gallery/photo5.jpg'),
      require('../../assets/gallery/photo6.jpg'),
      require('../../assets/gallery/photo7.jpg'),
      require('../../assets/gallery/photo8.jpg')
    ],
    index: null
  }),

  methods: {
    exitSheet () {
      const active = false
      this.$emit('sheetDel', active)
    }
  }
}
</script>

<style scoped lang="scss">
.wrapper {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(10px);
  z-index: 4;
  transition: 2s;
  padding-top: 120px;
  .wrap {
    position: relative;
    .exit {
      position: absolute;
      top: 30px;
      right: 30px;
      cursor: pointer;
      z-index: 10;
      i {
        font-size: 30px;
        color: #fff;
      }
    }
  }
}
.gallery {
  margin-top: 100px;
}
.image {
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  border: 1px solid #ebebeb;
  cursor: pointer;
  margin: 5px 10px;
  width: 250px;
  height: 250px;
}
.max-height {
  height: 80vh;
  overflow-y: scroll;
}
.fade-enter {
  opacity: 0;
}
.fade-enter-active {
  transition: opacity 0.3s;
}
/* .fade-leave {

} */
.fade-leave-active {
  transition: opacity 0.3s;
  opacity: 0;
}

@media (max-width: 840px) {
  .image {
    width: 200px;
    height: 200px;
  }
}
@media (max-width: 480px) {
  .image {
    width: 150px;
    height: 150px;
  }
}
</style>
