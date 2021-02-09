<template>
  <div class="wrap">
    <div class="container">
      <div class="row">
        <img src="../../assets/Beach.png" alt>
        <div class="col-10 col-md-7 mx-auto">
          <h1>Chcesz doskonale pływać? Nie zwlekaj, zapisz się na zajęcia!</h1>
        </div>
        <ContactForm />
      </div>
    </div>
  </div>
</template>
<script>
import ContactForm from '../ContactForm/ContactFormComponent'
export default {
  components: {
    ContactForm
  }
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
    margin-bottom: 250px;
    color: #fff;
    text-align: center;
  }
  .row {
    display: flex;
    padding-top: 150px;
  }
  img {
    position: absolute;
    top: 400px;
    width: 90%;
    max-width: 600px;
  }
}
</style>
