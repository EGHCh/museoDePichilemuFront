<template>
  <div class="container-fluid editorial-modal mt-sm-5 fixed-bottom d-flex">
    <div class="modal-container py-4 px-2">
      <h3 class="modal-title">{{editorialTitle}}</h3>
      <hr />
      <p class="pb-4 px-sm-4">
        {{editorialBody}}
      </p>
      <button class="modal-close" @click="closeModal">
        <img src="../assets/close.png" alt="" />
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalEditorial",
  props: {
    editorialTitle: String,
    editorialBody: String
  },
  methods: {
    closeModal: function () {
      document.querySelector(".editorial-modal").classList.add("d-none");
      document.querySelector(".editorial-modal").classList.remove("d-flex");
    },
  },
};
</script>

<style>
.editorial-modal {
  box-sizing: border-box;
  top: 0;
  width: 100vw;
  height: 100vh;
  z-index: 1999;
  background-color: rgba(0, 0, 0, 0.5);
  align-items: center;
  justify-content: center;
  font-family: "Old Standard TT", serif;
}
.editorial-modal .modal-container {
  height: 70vh;
  max-width: 700px;
  background-image: url(https://images.unsplash.com/photo-1615800098779-1be32e60cca3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2020&q=80);
  background-attachment: fixed;
}
.editorial-modal .modal-container .modal-title {
  font-size: 24px;
  font-weight: bold;
  line-height: 24px;
}
.editorial-modal .modal-container p {
  max-height: 70%;
  overflow: scroll;
}
.editorial-modal .modal-close {
  border: none;
  background: rgba(0, 0, 0, 0);
}
</style>
