<template>
  <div class="col-10 col-sm-8 col-md-5 mx-auto mb-5 sheets">
    <img :src="skillimg" alt="Photo not loaded">
    <h4>{{ textOnSkill }}</h4>
    <p>{{ textOnSkillBottom }}</p>
  </div>
</template>

<script>
export default {
  props: {
    skillimg: {
      type: String,
      default: ''
    },
    textOnSkill: {
      type: String,
      default: ''
    },
    textOnSkillBottom: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.sheets {
  border: 5px solid #2fc0df;
  border-radius: 30px;
  color: black;
  background-color: #fff;

  > img {
    width: 70%;
    margin: 35px 20px 30px;
  }
  > h4 {
    color: #102c4f;
    height: 60px;
    margin-bottom: 20px;
  }
  > p {
    text-align: justify;
    margin: 0 auto;
    margin-bottom: 30px;
    width: 90%;
  }
}
</style>
