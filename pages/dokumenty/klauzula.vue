<template>
  <div class="pdfContainer">
    <h2 class="mb-4">
      Klauzula informacyjna - dane osobowe
    </h2>
    <p class="mb-2 text-right link">
      <a href="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW.pdf" download="">Pobierz <i class="fas fa-download" /></a>
    </p>
    <div class="terms">
      <img src="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW1024_1.jpg" alt="Zasady użytkowania strony Swim or Sink strona 1">
      <img src="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW1024_2.jpg" alt="Zasady użytkowania strony Swim or Sink strona 2">
      <img src="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW1024_3.jpg" alt="Zasady użytkowania strony Swim or Sink strona 3">
      <img src="/terms/ZasadyUzytkowaniaStronyWWW/ZasadyUzytkowaniaStronyWWW1024_4.jpg" alt="Zasady użytkowania strony Swim or Sink strona 4">
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
