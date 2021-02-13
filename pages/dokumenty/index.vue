<template>
  <div class="pdfContainer">
    <h2 class="mb-4">
      Dokumenty
    </h2>
    <h5 class="mb-4">
      Klauzula informacyjna - RODO
    </h5>
    <p class="mb-2 text-right link">
      <a href="/terms/RODOSwimOrSink/RODOSwimOrSink.pdf" download="">Pobierz <i class="fas fa-download" /></a>
    </p>
    <!-- konto gmail SOS -->
    <!-- <iframe src="https://drive.google.com/file/d/1EaQ9tcZb3gvHJgbnCA9n2CjtJuy_E8pC/preview" class="pdf" /> -->
    <div class="terms">
      <img src="/terms/RODOSwimOrSink/RODOSwimOrSink1024_1.jpg" alt="Rodo Swim or Sink strona 1">
      <img src="/terms/RODOSwimOrSink/RODOSwimOrSink1024_2.jpg" alt="Rodo Swim or Sink strona 2">
      <img src="/terms/RODOSwimOrSink/RODOSwimOrSink1024_3.jpg" alt="Rodo Swim or Sink strona 3">
    </div>
    <h5 class="mb-4">
      Regulamin uczestnictwa
    </h5>
    <p class="mb-2 text-right link">
      <a href="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink.pdf" download="">Pobierz <i class="fas fa-download" /></a>
    </p>
    <!-- konto gmail SOS -->
    <!-- <iframe src="https://drive.google.com/file/d/1EZd2SxiBX5nQcWDL0mDjUSnLKbylsNHR/preview" class="pdf" /> -->
    <div class="terms">
      <img src="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink1024_1.jpg" alt="Regulamin Swim or Sink strona 1">
      <img src="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink1024_2.jpg" alt="Regulamin Swim or Sink strona 2">
      <img src="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink1024_3.jpg" alt="Regulamin Swim or Sink strona 3">
      <img src="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink1024_4.jpg" alt="Regulamin Swim or Sink strona 4">
      <img src="/terms/RegulaminSwimOrSink/RegulaminSwimOrSink1024_5.jpg" alt="Regulamin Swim or Sink strona 5">
    </div>
  </div>
</template>
<style scoped lang="scss">
.pdfContainer {
  max-width: 1000px;
  padding: 1rem;
  margin: 120px auto 0;

  .link a {
      color: #2d3681;
      transition: 0.25s;

      &:hover {
        color: #2fc0df;
      }

      &focus {
        color: #2d3681;
      }
  }

  .pdf {
    width: 100%;
    height: 70vh;
    margin-bottom: 2rem;
  }

  .terms {
    width: 100%;
    padding: 1rem;
    background-color: lightgray;
    margin-bottom: 4rem;

    img {
      margin-bottom: 1rem;
      width: 100%;
      height: auto;

      &:last-of-type {
        margin-bottom: 0rem;
      }
    }
  }
}
</style>
