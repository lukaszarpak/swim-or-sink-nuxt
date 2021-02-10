<template>
  <div class="pdfContainer">
    <h2 class="mb-4">
      Dokumenty
    </h2>
    <h5 class="mb-4">
      Klauzula informacyjna RODO
    </h5>
    <p class="mb-2 text-right link">
      <a href="/terms/RODOSwimOrSink.pdf" download="">Pobierz <i class="fas fa-download" /></a>
    </p>
    <!-- <embed src="/terms/RegulaminSwimOrSink.pdf" class="pdf">
    <embed src="/terms/RODOSwimOrSink.pdf" class="pdf"> -->
    <iframe src="https://drive.google.com/file/d/1hNSAREeHT_vwGDmpx4Y4BU87ENvNxCqZ/preview" class="pdf" />
    <h5 class="mb-4">
      Regulamin uczestnictwa
    </h5>
    <p class="mb-2 text-right link">
      <a href="/terms/RegulaminSwimOrSink.pdf" download="">Pobierz <i class="fas fa-download" /></a>
    </p>
    <iframe src="https://drive.google.com/file/d/1b8_qQvkcopaSI72VefDzNDR7CpS8DaFm/preview" class="pdf" />
  </div>
</template>
<style scoped lang="scss">
.pdfContainer {
  max-width: 1400px;
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
}
</style>
