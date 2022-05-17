<template>
  <section
    class="editorial-links container-fluid d-flex justify-content-around mx-2 mx-sm-5"
  >
    <a href="" class=" col-sm-5 text-sm-center editorial-links__link">Editorial</a>
    <div class="vr d-none d-sm-flex"></div>
    <a
      href=""
      data-bs-target="#myModal"
      data-bs-toggle="modal"
      class="col-8 col-sm-5 text-sm-center editorial-links__link"
      >Qué entendemos por patrimonio cultural</a
    >
  </section>
  <!-- MODAL -->
</template>

<script>
export default {
  name: "EditorialSection",
};
</script>

<style>
.editorial-links {
  margin-top: 1rem;
  border-bottom: 1.5px solid #1d1d1d;
}
.editorial-links .editorial-links__link {
  font-family: "Old Standard TT", serif;
  font-weight: bold;
  text-decoration: none;
  color: #1d1d1d;
  font-size: 20px;
}
@media (max-width: 992px) {
  .editorial-links .editorial-links__link {
    font-size: 16px;
    font-weight: normal;
  }
}
</style>
