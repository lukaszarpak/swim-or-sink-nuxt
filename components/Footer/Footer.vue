<template>
  <div class="wrap">
    <div class="container">
      <div class="row">
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot icons">
          <a href="https://www.facebook.com/SwimOrSink.SzkolaPlywania/" target="_blank">
            <i class="fab fa-facebook-square" />
          </a>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <div>
            <p>Dane kontaktowe:</p>
            <p>Swim or Sink - Kamil Szulik</p>
          </div>
          <div>
            <p>ul. Julianowska 72e/22</p>
            <p>05-500 Julianów</p>
            <p>NIP 123-113-72-02</p>
          </div>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p><a href="tel:+48517507819" style="text-decoration: underline;">tel. Kamil 517-507-819</a></p>
          <p><a href="tel:+48793522535" style="text-decoration: underline;">tel. Kuba 793-522-535</a></p>
          <p><a href="mailto:szkolaplywaniasos@gmail.com" style="text-decoration: underline;">e-mail: szkolaplywaniasos@gmail.com</a></p>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p><a href="/terms/RODOSwimOrSink/RODOSwimOrSink.pdf" style="text-decoration: underline;" target="_blank">RODO</a></p>
          <p><a href="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink.pdf" style="text-decoration: underline;" target="_blank">Regulamin</a></p>
          <p>Design i wykonanie</p>
          <p><a href="https://www.lukaszarpak.com/" target="_blank" style="text-decoration: underline;">lukaszarpak.com</a></p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
.wrap {
  background-color: #0b1f37;
  padding: 50px 0 0 0;
}
.row {
  display: flex;
  align-items: center;
}
.foot {
  padding-bottom: 30px;
  color: #fff;
  p {
    text-align: center;
    a {
      color: #fff;
    }
  }
}
.icons {
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
  a {
    i {
      color: #fff;
      font-size: 60px;
      margin: 0 20px;
      transition: 0.15s;
    }
    i:hover {
      color: #0b70b8;
    }
  }
}
</style>
