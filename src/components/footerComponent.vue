<template>
  <footer class="container-fluid footer fixed-bottom text-center d-flex justify-content-center">
    <div class="col-11 d-flex"><p>Una produccion de <a class="footer__link" href="http://www.pichilemunews.cl/" target="_blank">www.pichilemunews.cl</a></p></div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style>
.footer {
  font-family: "Old Standard TT", serif;
  font-size: 24px;
  text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.1);
  background-image: url(https://images.unsplash.com/photo-1615800098779-1be32e60cca3?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2020&q=80);
  
}
.footer div {
  
  border-top: 1.5px solid #1d1d1d;
  justify-content: center;
  align-items: center;
  padding: .5rem;
}
.footer p {
  margin-bottom: 0;
}
.footer a {
  text-decoration: none;
  font-family: 'Roboto mono',sans-serif;
  font-style: italic;
  font-size: 22px;
}
</style>
