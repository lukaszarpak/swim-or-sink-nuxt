<template>
  <div class="wrap">
    <h2>Kontakt</h2>
    <div class="container">
      <div class="row">
        <div class="col-10 col-md-5 mx-auto firstRow">
          <h3>Zainteresowała Cię nasza oferta?</h3>
          <p
            style="margin-bottom: 40px;"
          >
            Wypełnij formularz po prawej stronie, a my odpiszemy lub oddzwonimy do Ciebie najszybciej jak to możliwe.
          </p>
          <p>Nasz e-mail:</p>
          <p style="font-weight: bold; margin-bottom: 40px">
            szkolaplywaniasos@gmail.com
          </p>
          <p>Telefon:</p>
          <p style="font-weight: bold">
            517-507-819
          </p>
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
  background-color: #102c4f;
  color: #fff;
  padding: 100px 0 100px;
  .firstRow {
    margin-bottom: 80px;
  }
  h2 {
    text-align: center;
    margin-bottom: 90px;
  }
  .row {
    > div {
      h3 {
        color: #2fc0df;
        margin: 0 0 30px;
      }
      p {
        margin-bottom: 15px;
      }
    }
  }
}
</style>
