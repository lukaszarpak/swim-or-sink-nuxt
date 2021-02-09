<template>
  <div class="col-10 col-md-7 col-lg-5 mx-auto mb-5 trainer">
    <img :src="trainerPhoto" alt="Photo not loaded">
    <h3>{{ trainerName }}</h3>
    <p>{{ trainerDescription }}</p>
  </div>
</template>

<script>
export default {
  props: {
    trainerPhoto: {
      type: String,
      default: ''
    },
    trainerName: {
      type: String,
      default: ''
    },
    trainerDescription: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.trainer {
  border: 5px solid #2fc0df;
  border-radius: 30px;
  color: black;
  background-color: #fff;

  &:hover {
    img {
      box-shadow: 5px 5px 15px 8px rgba(80, 80, 80, 0.226);
      width: 80%;
    }
    h3 {
      margin-top: 30px;
    }
  }

  > img {
    width: 90%;
    margin: 35px auto 30px;
    border-radius: 20px;
    transition: 0.5s;
  }
  > h3 {
    color: #102c4f;
    margin-bottom: 20px;
    transition: 0.5s;
  }
  > p {
    text-align: justify;
    margin: 0 auto;
    margin-bottom: 30px;
    width: 90%;
  }
}
</style>
