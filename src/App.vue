<template>
  <div class="container-fluid main">
    <NavbarComponent></NavbarComponent>
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
