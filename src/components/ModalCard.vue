<template>
  <div class="container-fluid card-modal mt-sm-5 fixed-bottom d-none">
    <div class="modal-container py-4 px-2">
      <img src="{{modalSRC}}" alt="" />
      <div>
        <h3 class="modal-title">{{ modalTitle }}</h3>
        <hr />
        <p class="pb-4 px-sm-4">
          {{ modalBody }}
        </p>
        <button class="modal-close" @click="closeModal">
          <img src="../assets/close.png" alt="" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ModalCard",

  props: {
    modalSRC: String,
    modalTitle: String,
    modalBody: String,
  },
  methods: {
    closeModal: function () {
      document.querySelector(".card-modal").classList.add("d-none");
      document.querySelector(".card-modal").classList.remove("d-flex");
    },
  },
};
</script>

<style>
.card-modal {
  box-sizing: border-box;
  top: 0;
  width: 100vw;
  height: 100vh;
  z-index: 1999;
  background-color: rgba(0, 0, 0, 0.5);
  align-items: center;
  justify-content: center;
  font-family: "Roboto Mono", monospace;
}
.card-modal .modal-container {
  height: 70vh;
  width: 80vw;
  max-width: 700px;
  background-color: rgb(233, 138, 21);
  background-attachment: fixed;
}
.card-modal .modal-title {
  font-size: 24px;
  font-weight: bold;
  line-height: 24px;
}
.card-modal .modal-container p {
  max-height: 70%;
  overflow: scroll;
}
.card-modal .modal-close {
  border: none;
  background: rgba(0, 0, 0, 0);
}
</style>
