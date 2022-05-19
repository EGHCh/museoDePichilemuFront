<template>
  <div class="FAB"></div>
</template>

<script>
export default {
  name: "FAB",
};
</script>

<style>
.show-FAB {
  width: 50px;
  height: 50px;
  background-color: aqua;
  bottom: 20%;
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
