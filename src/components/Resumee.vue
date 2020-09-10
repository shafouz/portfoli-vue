<template>
  <div class="container text-center">
    <h1>Resumee</h1>
    <embed
      src="portfolio.pdf"
      type="application/pdf"
      class="pdf-embed"
      />
      <hr class="m-0">
  </div>
</template>

<script>
export default {
  name: 'resumee',
}
</script>

<style>
.pdf-embed {
  width: 90%;
  height: 50rem;
  padding-bottom: 3rem; 
}
</style>
