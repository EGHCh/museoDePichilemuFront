<template>
  <section class="editorial-links container-fluid d-flex justify-content-around mx-5">
    <a href="" class="col-5 text-center editorial-links__link">Editorial</a>
    <div class="vr"></div>
    <a href="" data-bs-toggle="modal" class="col-5 text-center editorial-links__link">Qué entendemos por patrimonio cultural</a>
  </section>
</template>

<script>
export default {
  name: "EditorialSection",
}
</script>

<style>
.editorial-links {
  border-bottom: 1.5px solid #1d1d1d;
}
  .editorial-links .editorial-links__link{
    font-family: 'Old Standard TT', serif;
    text-decoration: none;
    color: #1d1d1d;
    font-size: 24px;
  }
</style>