<script>
  export let urlImage = "assets/poco.png";
</script>

<style>
  section {
    padding: 0 20%;
  }

  .header {
    height: 500px;
    width: 100%;
    background-repeat: no-repeat;
    background-size: contain;
    background-position: center center;
  }
</style>

<section>
  <h1 class="center">Detalhes</h1>

  <div class="header" style={"background-image: url('" + urlImage + "')"} />
  <h2 class="center name">Lorem ipsum dolor</h2>
  <p class="infos">
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat adipisci
    doloremque repudiandae incidunt doloribus impedit qui? Ullam debitis animi
    esse, explicabo nemo harum eveniet minima recusandae error earum sint
    sapiente.
  </p>
  <p class="infos">
    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Eveniet laudantium, ad nostrum esse cumque, nesciunt vero laboriosam deserunt itaque dolor molestias ex totam consectetur praesentium, et quidem ipsum quaerat sit.
  </p>
  <p class="infos">
    Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quam unde at delectus. Eum voluptates voluptas illum, deserunt temporibus culpa ipsum deleniti incidunt aliquid saepe numquam! Laudantium quidem impedit voluptatem consequatur.
  </p>
</section>
