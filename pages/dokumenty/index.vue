<template>
  <div class="pdfContainer">
    <h2 class="mb-4">
      Dokumenty
    </h2>
    <embed src="/terms/RegulaminSwimOrSink.pdf" class="pdf">
    <embed src="/terms/RODOSwimOrSink.pdf" class="pdf">
  </div>
</template>
<style scoped lang="scss">
.pdfContainer {
  max-width: 1400px;
  padding: 1rem;
  margin: 120px auto 0;

  .pdf {
    width: 100%;
    height: 70vh;
    margin-bottom: 2rem;
  }
}
</style>
