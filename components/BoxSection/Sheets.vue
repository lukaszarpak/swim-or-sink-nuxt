<template>
  <div class="wrapper" @click="exitSheet">
    <div class="sheet">
      <div class="exit" @click="exitSheet">
        <i class="fas fa-times"></i>
      </div>
      <div class="content">
        <slot name="title"></slot>
        <slot name="day1"></slot>
        <slot name="description1"></slot>
        <slot name="day2"></slot>
        <slot name="description2"></slot>
        <slot name="day3"></slot>
        <slot name="description3"></slot>
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
  position: fixed !important;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.4);
  backdrop-filter: blur(10px);
  z-index: 4;
  transition: 2s;
  color: #2d3681;
  .sheet {
    position: relative;
    top: 55%;
    left: 50%;
    transform: translate(-50%, -50%);
    background-color: #fff;
    max-width: 800px;
    width: 90%;
    max-height: 700px;
    border-radius: 30px;
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
