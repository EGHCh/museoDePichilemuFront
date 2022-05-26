<template>
  <EditorialSection class="sticky-top d-sm-none editorial-for-mobile pt-2" />
  <div :v-for="(post, index) in posts">
    <p>{{ posts }}</p>
  </div>
  <section class="gallery container-fluid d-flex">
    <div
      class="gallery__selector fixed-left gallery__selector--desktop gallery__selector--left d-flex flex-column mx-auto"
    >
      <a href="" class="text-center">A</a>
      <a href="" class="text-center">B</a>
      <a href="" class="text-center">C</a>
      <a href="" class="text-center">D</a>
      <a href="" class="text-center">E</a>
      <a href="" class="text-center">F</a>
      <a href="" class="text-center">G</a>
      <a href="" class="text-center">H</a>
      <a href="" class="text-center">I</a>
      <a href="" class="text-center">J</a>
      <a href="" class="text-center">K</a>
      <a href="" class="text-center">L</a>
      <a href="" class="text-center">M</a>
      <a href="" class="text-center">N</a>
    </div>
    <div
      @wheel="riseIndex"
      class="gallery__display container gallery__grid ms-3 ms-sm-auto"
    >
      <!-- <CardTemplate
        cardTitle="post.title"
        cardBody="post.body"
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
      >
      </CardTemplate> -->
    </div>
    <div
      class="gallery__selector gallery__selector--desktop gallery__selector--right d-flex flex-column mb-auto mt-auto"
    >
      <a href="" class="text-center">Ñ</a>
      <a href="" class="text-center">O</a>
      <a href="" class="text-center">P</a>
      <a href="" class="text-center">Q</a>
      <a href="" class="text-center">R</a>
      <a href="" class="text-center">S</a>
      <a href="" class="text-center">T</a>
      <a href="" class="text-center">U</a>
      <a href="" class="text-center">V</a>
      <a href="" class="text-center">W</a>
      <a href="" class="text-center">X</a>
      <a href="" class="text-center">Y</a>
      <a href="" class="text-center">Z</a>
    </div>
  </section>
</template>

<script>
// import CardTemplate from "./card.vue";
import EditorialSection from "./editorialSection.vue";

export default {
  name: "Gallery-section",
  components: {
    // CardTemplate,
    EditorialSection,
  },
  props: {
    posts: Array,
  },
  mounted() {
    console.log(this.posts);
  },
  methods: {},
};
</script>

<style>
CardTemplate {
  margin-bottom: 1rem;
}
.editorial-for-mobile {
  background-image: url(https://images.unsplash.com/photo-1615800098779-1be32e60cca3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2020&q=80);
  background-attachment: fixed;
  border-top: 1px solid black;
  border-bottom: 0;
}
.gallery__selector {
  font-family: "Old Standard TT", serif;
}
.gallery .gallery__selector {
  position: fixed;
}
.gallery__selector a {
  text-decoration: none;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.2);
  color: #1d1d1d;
  font-size: 20px;
  width: 30px;
}
.gallery__selector a:hover {
  font-size: 24px;
  color: #1d1d1d;
}
.gallery__selector--left {
  border-right: 1.5px solid #1d1d1d;
  left: 0;
}
.gallery__selector--right {
  border-left: 1.5px solid #1d1d1d;
  right: 0;
}
.gallery .gallery__display {
  width: auto;
}
.gallery .gallery__grid {
  display: grid;
  grid-template-columns: 300px;
  grid-gap: 1rem;
}
/* BREAKPOINTS */

@media (min-width: 576px) {
  .gallery__selector a {
    font-size: 24px;
    width: 40px;
  }
  .gallery__selector a:hover {
    font-size: 28px;
    color: #1d1d1d;
  }
}

@media (min-width: 724px) {
  .gallery .gallery__grid {
    grid-template-columns: 300px 300px;
    margin-left: auto;
  }
}
@media (min-width: 999px) {
  .gallery .gallery__grid {
    grid-template-columns: 300px 300px 300px;
  }
}
@media (min-width: 1400px) {
  .gallery .gallery__grid {
    grid-template-columns: 300px 300px 300px 300px;
  }
}
</style>
