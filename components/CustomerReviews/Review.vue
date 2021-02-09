<template>
  <div class="col-11 col-sm-10 col-md-8 col-lg-5 mx-auto review">
    <div class="topPart">
      <img :src="reviewimg" alt>
      <div class="description">
        <p>{{ nameOnReview }}</p>
        <i class="fas fa-star" />
        <i class="fas fa-star" />
        <i class="fas fa-star" />
        <i class="fas fa-star" />
        <i class="fas fa-star" />
      </div>
    </div>
    <p>{{ textOnReview }}</p>
  </div>
</template>

<script>
export default {
  props: {
    reviewimg: {
      type: String,
      default: ''
    },
    nameOnReview: {
      type: String,
      default: ''
    },
    textOnReview: {
      type: String,
      default: ''
    }
  }
}
</script>

<style lang="scss" scoped>
.review {
  border-radius: 30px;
  box-shadow: 5px 5px 15px 8px rgba(199, 199, 199, 0.36);
  padding: 30px;
  margin: 30px 0;
  text-align: left;
  transition: box-shadow 0.3s;
  &:hover {
    box-shadow: 5px 5px 15px 8px rgba(173, 173, 173, 0.36);
  }
  .topPart {
    display: flex;
    img {
      width: 80px;
      height: 80px;
      margin-right: 30px;
      background-color: grey;
      border-radius: 50%;
    }
    .description {
      margin: 10px 0;
      p {
        margin: 0 0 10px 0;
        font-size: 1.2rem;
      }
      i {
        color: gold;
        margin-right: 10px;
      }
    }
  }
  > p {
    margin: 20px 0 0 0;
    padding: 0;
    text-align: justify;
  }
}
</style>
