<template>
  <div class="wrapper" @click="exitSheet">
    <div class="sheet">
      <div class="exit" @click="exitSheet">
        <i class="fas fa-times" />
      </div>
      <div class="content">
        <slot name="title" />
        <slot name="day1" />
        <slot name="description1" />
        <slot name="day2" />
        <slot name="description2" />
        <slot name="day3" />
        <slot name="description3" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  methods: {
    exitSheet () {
      this.$emit('sheetDel', false)
    }
  }
}
</script>
<style lang="scss" scoped>
.wrapper {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(10px);
  transition: 2s;
  color: #2d3681;
  .sheet {
    position: fixed;
    top: 50%;
    left: 50%;
    z-index: 10;
    transform: translate(-50%, -50%);
    background-color: #fff;
    max-width: 800px;
    width: 90%;
    max-height: 500px;
    overflow-y: scroll;
    border-radius: 30px;

    @media(max-width: 400px) {
      top: 55%;
      max-height: 450px;
    }
    @media(min-width: 700px) {
      max-height: 700px;
    }

    .exit {
      position: absolute;
      top: 30px;
      right: 30px;
      cursor: pointer;
      i {
        font-size: 30px;
      }
    }
    .content {
      width: 90%;
      height: 100%;
      padding: 50px 0;
      margin: 0 auto;
      text-align: left;
      h2 {
        margin-bottom: 20px;
      }
      h3 {
        margin-top: 15px;
        font-size: 1.5rem;
      }
      p {
        margin-bottom: 2px;
      }
    }
  }
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
</style>
