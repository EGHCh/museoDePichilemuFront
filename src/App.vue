<template>
  <main class="container-fluid main">
    <!-- Modals -->
    <ModalPatrimonio class="d-none" />
    <ModalEditorial class="d-none" />
    <!-- Site Body -->
    <NavbarComponent
      @wheel="riseIndex"
      class="d-sm-none p-0 mb-0 mobile-navbar"
    />
    <FAB @click="backToTheNavbar" />
    <NavbarComponent class="fixed-top d-none d-sm-flex" />
    <GallerySection :posts="data"></GallerySection>
    <FooterComponent></FooterComponent>
  </main>
</template>

<script>
import { ref } from "vue";
import axios from "axios";
import NavbarComponent from "./components/navbar.vue";
import GallerySection from "./components/gallery.vue";
import FooterComponent from "./components/footerComponent.vue";
import FAB from "./components/FAB.vue";
import ModalPatrimonio from "./components/ModalPatrimonio.vue";
import ModalEditorial from "./components/ModalEditorial.vue";

export default {
  setup() {
    const result = ref(null);

    return { result };
  },
  name: "App",
  components: {
    NavbarComponent,
    GallerySection,
    FooterComponent,
    FAB,
    ModalPatrimonio,
    ModalEditorial,
  },
  data () {
    return {
      data: [],
    }
  },
  mounted(){
    axios
      .get("http://jsonplaceholder.typicode.com/posts")
      .then((data) => (this.data = data));
  },
  methods: {
    holi: function (e) {
      console.log(e);
    },
    riseIndex: function () {
      document
        .querySelector(".main .navbar")
        .classList.add("mobile-navbar--vanish");
      document.querySelector(".main .FAB").classList.add("show-FAB");
      document.querySelector(".main .FAB").classList.remove("d-none");
    },
    backToTheNavbar: function () {
      document
        .querySelector(".main .navbar")
        .classList.remove("mobile-navbar--vanish");
      document.querySelector(".main .FAB").classList.add("d-none");
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
