<script>
  import Home from "../views/Home.svelte";
  import Brawls from "../views/Brawls.svelte";
  import Details from "../views/Details.svelte";
  import Contact from "../views/Contact.svelte";

  let currentPage = "home";

  function toPage(page) {
    currentPage = page;
  }
</script>

<style>
  #main {
    display: flex;
  }
  .sidenav {
    height: 100vh;
    width: 260px;
    background-color: #111;
    overflow-x: hidden;
    padding-top: 20px;
  }
  .sidenav button {
    font-size: 22px;
    color: #000000;
    width: 100%;
    padding: 8px 10px;
    display: block;
    margin: 10px auto;
  }

  .sidenav button:hover {
    color: #f1f1f1;
  }

  .sidenav .logo {
    height: 15%;
  }
</style>

<div id="main">
  <div class="sidenav">
    <img class="logo centralizado" src="assets/logo.jpg" alt="Brawl Starts" />
    <button
      class:active={currentPage === 'home'}
      on:click={() => {
        toPage('home');
      }}>
      Home
    </button>
    <button
      class:active={currentPage === 'brawls'}
      on:click={() => {
        toPage('brawls');
      }}>
      Brawls
    </button>
    <button
      class:active={currentPage === 'details'}
      on:click={() => {
        toPage('details');
      }}>
      Detalhes
    </button>
    <button
      class:active={currentPage === 'contact'}
      on:click={() => {
        toPage('contact');
      }}>
      Contact
    </button>
  </div>

  {#if currentPage === 'home'}
    <Home />
  {:else if currentPage === 'brawls'}
    <Brawls />
  {:else if currentPage === 'details'}
    <Details />
  {:else if currentPage === 'contact'}
    <Contact />
  {/if}
</div>
