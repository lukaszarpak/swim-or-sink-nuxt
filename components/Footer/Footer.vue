<template>
  <div class="wrap">
    <div class="container">
      <div class="row">
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p class="font-weight-bold">
            Informacje
          </p>
          <hr>
          <p>Swim or Sink - Kamil Szulik</p>
          <p>NIP 123-113-72-02</p>
          <p>ul. Julianowska 72e/22<br>05-500 Julianów</p>
          <a href="https://www.facebook.com/SwimOrSink.SzkolaPlywania/" target="_blank" class="icon">
            <i class="fab fa-facebook-square" />
          </a>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p class="font-weight-bold">
            Numer konta bankowego
          </p>
          <hr>
          <p>87 1870 1045 2078 1065 8610 0001</p>
          <p>* W tytule przelewu prosimy o podanie Imienia i Nazwiska uczestnika oraz dnia i godziny zajęć.</p>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p class="font-weight-bold">
            Dane kontaktowe:
          </p>
          <hr>
          <p><a href="tel:+48517507819">tel. Kamil 517-507-819</a></p>
          <p><a href="tel:+48793522535">tel. Kuba 793-522-535</a></p>
          <p><a href="mailto:szkolaplywaniasos@gmail.com">e-mail: szkolaplywaniasos@gmail.com</a></p>
        </div>
        <div class="col-10 col-sm-6 col-lg-3 mx-auto foot">
          <p class="font-weight-bold">
            Dokumenty:
          </p>
          <hr>
          <p><a href="/terms/RODOSwimOrSink/RODOSwimOrSink.pdf" target="_blank">Klauzula informacyjna - RODO</a></p>
          <p><a href="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW.pdf" target="_blank">Klauzula informacyjna - dane osobowe</a></p>
          <p><a href="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink.pdf" target="_blank">Regulamin uczestnictwa</a></p>
          <p><a href="/terms/PolitykaCookies/PolitykaCookies.pdf" target="_blank">Informacje o plikach cookies</a></p>
        </div>
      </div>
    </div>
    <a href="https://www.lukaszarpak.com/" target="_blank" class="credentials">
      <span class="credentials__inner">
        <span>Design i wykonanie: </span>
        <span>Łukasz Szarpak</span>
      </span>
    </a>
  </div>
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
.wrap {
  background-color: #0b1f37;
  padding: 50px 0 0 0;

  .credentials {
    display: block;
    background-color: #ff0066;
    margin: 0;
    padding: 0.25rem 2rem;
    color: white;
    text-decoration: none;

    .credentials__inner {
      display: flex;
      max-width: 1140px;
      margin: 0 auto;
      justify-content: space-between;
      align-items: center;

    }
  }
}
.foot {
  padding-bottom: 30px;
  color: #fff;
  hr {
    border: 1px solid white;
  }
  a {
    color: #fff;

    &.icon i {
      font-size: 40px;
      transition: 0.15s;

      &:hover {
        color: #0b70b8;
      }
    }
  }
}
</style>
