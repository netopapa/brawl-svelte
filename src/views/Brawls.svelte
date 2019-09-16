<script>
  import { createEventDispatcher } from "svelte";
  import Details from "./Details.svelte";

  const dispatch = createEventDispatcher();

  function showDetails(urlImage) {
    dispatch("detail", urlImage);
  }
</script>

<style>
  .brawl-list {
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .brawl-item {
    cursor: pointer;
    width: 320px;
    background-color: #fff;
    border-radius: 5px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    box-shadow: 4px 4px 6px #8e8e8e;
    transition: 0.2s linear;
  }

  .brawl-item:hover {
    transform: scale(1.02);
  }

  .brawl-item .header {
    height: 400px;
    width: 100%;
    background-repeat: no-repeat;
    background-size: 50%;
    background-position: center center;
  }

  .brawl-item .name {
    width: 100%;
  }

  .brawl-item .infos {
    padding: 10px;
  }
</style>

<section>
  <h1 class="center">Lista de Personagens</h1>

  <div class="brawl-list">

    <div
      class="brawl-item"
      on:click={() => {
        showDetails('assets/leon.png');
      }}>
      <div class="header" style="background-image: url('assets/leon.png')" />
      <h3 class="center name">Lorem ipsum dolor</h3>
      <p class="infos">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur,
        deleniti. Consequuntur eius animi sunt natus aut aperiam.
      </p>
    </div>

    <div
      class="brawl-item"
      on:click={() => {
        showDetails('assets/barley.png');
      }}>
      <div class="header" style="background-image: url('assets/barley.png')" />
      <h3 class="center name">Lorem ipsum dolor</h3>
      <p class="infos">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur,
        deleniti. Consequuntur eius animi sunt natus aut aperiam.
      </p>
    </div>

    <div
      class="brawl-item"
      on:click={() => {
        showDetails('assets/poco.png');
      }}>
      <div class="header" style="background-image: url('assets/poco.png')" />
      <h3 class="center name">Lorem ipsum dolor</h3>
      <p class="infos">
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Consequuntur,
        deleniti. Consequuntur eius animi sunt natus aut aperiam.
      </p>
    </div>

  </div>
</section>
