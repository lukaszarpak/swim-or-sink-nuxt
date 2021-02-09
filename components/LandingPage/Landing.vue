<template>
  <div class="wrap">
    <div class="container">
      <div class="row">
        <img src="../../assets/Beach.png" alt>
        <div class="col-10 col-md-7 mx-auto">
          <h1>Chcesz doskonale pływać? Nie zwlekaj, zapisz się na zajęcia!</h1>
          <nuxt-link to="/zapisy" class="linkBtn">
            Zapisy
          </nuxt-link>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
}
</script>
<style lang="scss" scoped>
.wrap {
  background: linear-gradient(
    180deg,
    rgba(45, 54, 129, 1) 0%,
    rgba(16, 44, 79, 1) 100%
  );
}
.container {
  padding: 100px 0;

  h1 {
    margin-bottom: 25px;
    color: #fff;
    text-align: center;
  }
  .row {
    display: flex;
    padding-top: 150px;
    margin-bottom: 200px;
  }
  img {
    position: absolute;
    top: 470px;
    width: 100%;

    @media screen and (min-width: 670px) {
      top: 350px;
      width: 90%;
      max-width: 1000px;
    }

    @media screen and (min-width: 900px) {
      top: 200px;
      width: 90%;
      max-width: 1000px;
    }
  }
  .linkBtn {
    display: block;
    margin: 0 auto;
    color: #fff;
    background: none;
    border: 2px solid #fff;
    border-radius: 30px;
    padding: 10px 20px;
    width: 200px;
    font-weight: 700;
    text-align: center;
    text-decoration: none;
    font-size: 20px;
    transition: 0.2s;
    &:hover {
      background: #fff;
      color: #ff0066;
    }
    &:focus {
      outline: none;
    }
  }
}
</style>
