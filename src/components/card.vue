<template>
  <div class="">
    <div class="card">
      <img :src="picture_src" class="card-img-top" :alt="cardTitle" />
      <div class="card-body">
        <h5 class="card-title">{{ cardTitle }}</h5>
        <p class="card-text">
          {{ cardBody }}
        </p>
      </div>
    </div>
  </div>
  <ModalCard :modalSRC="picture_src" :modalTitle="cardTitle" :modalBody="cardBody"/>
</template>

<script>
import ModalCard from "./ModalCard.vue";

export default {
  name: "cardTemplate",
  components: {
    ModalCard,
  },
  props: {
    picture_src: String,
    cardTitle: String,
    cardBody: String,
  },
};
</script>

<style>
.card {
  max-width: 260px;
  height: 360px;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  cursor: pointer;
  margin-bottom: 1rem;
}
.card .card-img-top {
  height: 50%;
  object-fit: cover;
}
.card .card-body {
  font-family: "Roboto Mono", monospace;
  background-color: rgba(233, 138, 21, 0.5);
  overflow: hidden;
  text-overflow: ellipsis;
}
.card .card-title {
  font-size: 25px;
  line-height: 33px;
}
.card .card-text {
  font-size: 14px;
  line-height: 18px;
}

@media (min-width: 400px) {
  .card {
    width: 18rem;
  }
}
</style>
