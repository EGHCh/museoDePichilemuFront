<template>
  <section
    class="editorial-links container-fluid d-flex justify-content-around mx-1 mx-sm-5"
  >
    <button
      @click="openModalEditorial"
      class="col-sm-5 text-sm-center editorial-links__link"
    >
      Editorial
    </button>
    <div class="vr d-none d-sm-flex"></div>
    <button
      @click="openModalPatrimonio"
      class="col-6 col-sm-5 text-center editorial-links__link"
    >
      Qué entendemos por patrimonio cultural
    </button>
  </section>
</template>

<script>
export default {
  name: "EditorialSection",
  methods: {
    openModalPatrimonio: function () {
      document.querySelector(".patrimonio-modal").classList.add("d-flex");
      document.querySelector(".patrimonio-modal").classList.remove("d-none");
    },
    openModalEditorial: function () {
      document.querySelector(".editorial-modal").classList.add("d-flex");
      document.querySelector(".editorial-modal").classList.remove("d-none");
    },
  },
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
  border: none;
  background: rgba(0, 0, 0, 0);
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
