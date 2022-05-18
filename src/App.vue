<template>
  <div class="container-fluid main">
    <NavbarComponent class="fixed-top d-none d-sm-flex"/>
    <NavbarComponent class="d-sm-none p-0 mb-0"/>
    <GallerySection></GallerySection>
    <FooterComponent></FooterComponent>
  </div>
</template>

<script>
import NavbarComponent from "./components/navbar.vue";
import GallerySection from "./components/gallery.vue";
import FooterComponent  from "./components/footerComponent.vue";

export default {
  name: "App",
  components: {
    NavbarComponent,
    GallerySection,
    FooterComponent,
  },
};
</script>
<style>
</style>
