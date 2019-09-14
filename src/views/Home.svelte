<style>
  .slider-wrap {
    width: 100%;
    height: calc(100vh - 70px);
    position: relative;
  }

  .single-slide {
    width: 100%;
    height: 100%;
    position: absolute;
    opacity: 0;
    animation: slider-animation;
    animation-duration: 15s;
    animation-iteration-count: infinite;
    animation-timing-function: ease-in-out;
    background-size: cover;
  }

  #slide-1 {
    background-color: red;
    background-image: url("assets/slide1.jpg");
  }
  #slide-2 {
    background-color: rebeccapurple;
    animation-delay: 5s;
    background-image: url("assets/slide2.jpg");
  }
  #slide-3 {
    background-color: orange;
    animation-delay: 10s;
    background-image: url("assets/slide3.png");
  }

  .about {
    padding: 40px;
  }

  h1 {
    font-size: 25px;
  }

  p {
    font-size: 20px;
  }

  @keyframes slider-animation {
    0% {
      opacity: 0;
    }
    6% {
      opacity: 1;
    }
    24% {
      opacity: 1;
    }
    40% {
      opacity: 0;
    }
    100% {
      opacity: 0;
    }
  }
</style>

<section>
  <div class="slider-wrap">
    <div class="single-slide" id="slide-1" />
    <div class="single-slide" id="slide-2" />
    <div class="single-slide" id="slide-3" />
  </div>

  <div class="about">
    <h1>Lorem ipsum dolor sit amet</h1>
    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis quo
      aliquam voluptates voluptate non, accusantium nisi iure, nobis ea culpa
      accusamus possimus ipsa, error sint. Tempore fugit quisquam culpa vitae.
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem, molestiae
      sapiente obcaecati sit laboriosam ducimus reprehenderit harum saepe,
      suscipit itaque excepturi doloremque tempore nisi. Minus sunt eius
      nesciunt iusto voluptatem?
    </p>
    <p>
      Lorem, ipsum dolor sit amet consectetur adipisicing elit. Perspiciatis
      officiis voluptatibus earum cupiditate vitae tempore, reprehenderit
      perferendis corrupti, laboriosam dolorum, vel laudantium! Tempora at,
      delectus similique fuga inventore veritatis aliquam. Lorem ipsum dolor,
      sit amet consectetur adipisicing elit. Magnam voluptate enim quo velit
      nihil doloremque blanditiis deserunt perferendis, neque possimus mollitia,
      sequi ipsa. Consequatur illum, beatae fugit dolor aut autem!
    </p>
  </div>
</section>
