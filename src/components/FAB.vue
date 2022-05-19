<template>
  <div class="FAB d-none">
    <a href="#nav">
      <img src="@/assets/icons8-slide-up-36(-hdpi).png" alt="Volver arriba">
    </a>
  </div>
</template>

<script>
export default {
  name: "FAB",
};
</script>

<style>
.show-FAB {
  bottom: 15%;
  right: 20px;
  position: fixed;
  z-index: 10;
  animation: showFAB 2s ease;
}
@keyframes showFAB {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
