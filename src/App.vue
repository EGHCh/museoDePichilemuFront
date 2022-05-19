<template>
  <main class="container-fluid main">
    <NavbarComponent
      @wheel="riseIndex"
      class="d-sm-none p-0 mb-0 mobile-navbar"
    />
    <FAB @click="backToTheNavbar"/>
    <NavbarComponent class="fixed-top d-none d-sm-flex" />
    <GallerySection></GallerySection>
    <FooterComponent></FooterComponent>
  </main>
</template>

<script>
import NavbarComponent from "./components/navbar.vue";
import GallerySection from "./components/gallery.vue";
import FooterComponent from "./components/footerComponent.vue";
import FAB from "./components/FAB.vue";

export default {
  name: "App",
  components: {
    NavbarComponent,
    GallerySection,
    FooterComponent,
    FAB,
  },
  methods: {
    riseIndex: function () {
      document
        .querySelector(".main .navbar")
        .classList.add("mobile-navbar--vanish");
      document
        .querySelector(".main .FAB")
        .classList.add("show-FAB");
      document
        .querySelector(".main .FAB")
        .classList.remove("d-none");
    },
    backToTheNavbar: function () {
      document.querySelector(".main .navbar").classList.remove("mobile-navbar--vanish");
      document
        .querySelector(".main .FAB")
        .classList.add("d-none");
      window.scrollTo(0, 0);
    },
  },
};
</script>
<style>
.mobile-navbar {
  height: 80vh;
  animation: vanish-header 3s ease;
}
.main .mobile-navbar--vanish {
  height: 0vh;
  top: -75vh;
  animation: riseGallery 2s ease;
}

@keyframes riseGallery {
  from {
    height: 30vh;
  }
  to {
    height: 0vh;
    top: -30vh;
  }
}
</style>
