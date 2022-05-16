<template>
  <section class="gallery container-fluid d-flex px-0">
    <div
      class="gallery__selector gallery__selector--left d-flex flex-column mb-auto mt-5"
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
    <div class="gallery__display container-fluid d-flex flex-wrap gap-4">
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
      <CardTemplate
        picture_src="https://images.unsplash.com/photo-1576838202385-c4436b685897?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8MTkzMHxlbnwwfHwwfHw%3D&auto=format&fit=crop&w=500&q=60"
        cardTitle="Lorem Ipsum"
        cardBody="Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda body Hola Carda "
      ></CardTemplate>
    </div>
    <div
      class="gallery__selector gallery__selector--right d-flex flex-column mb-auto mt-5"
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
import CardTemplate from "./card.vue";

export default {
  name: "Gallery-section",
  components: { CardTemplate },
};
</script>

<style>
.gallery__selector {
  font-family: "Old Standard TT", serif;
  position: fixed;
}
.gallery__selector a {
  text-decoration: none;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.2);
  width: 40px;
  color: #1d1d1d;
  font-size: 24px;
}
.gallery__selector--left {
  border-right: 1.5px solid #1d1d1d;
}
.gallery__selector--right {
  border-left: 1.5px solid #1d1d1d;
  right: 0;
}
.gallery .gallery__display {
  /* justify-content: space-evenly; */
  padding-right: 40px;
  padding-left: 50px;
}
</style>
