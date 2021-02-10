
<template>
  <div class="iframe-container">
    <h2 class="mb-4">
      Wybierz godzinę i grupę aby zapisać się na zajęcia
    </h2>
    <div class="activenow-container">
      <div class="activenow-table-container">
        <center><img src="https://www.activenow.io/assets/ripple.gif" width="100px"></center>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  head: {
    script: [
      { src: 'https://app.activenow.pl/external/signup_table/load_by_js?code=f6c06ac1cf4d1de85b1d661509a6bdf0&school_id=3604', async: true }
    ]
  }
}
</script>
<style scoped>
.iframe-container {
  max-width: 1400px;
  margin: 120px auto 50px;
  padding: 1rem;
}
.activenow-container {
  border: 2px solid #0b70b8;
  border-radius: 30px;
  padding: 2rem 1rem;
}
</style>
