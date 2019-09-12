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
  nav {
    background-color: #fff;
    padding: 10px 20px;
    height: 50px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.3);
  }

  nav .logo{
    height: 100%;
    transform: scaleX(1.2);
  }

  nav .navigation {
    display: flex;
    justify-content: flex-end;
    align-items: center;
  }

  nav .navigation button {
    padding: 8px 12px;
    background-color: transparent;
    border: 0;
    margin-right: 10px;
    display: inline-block;
    vertical-align: middle;
    -webkit-transform: perspective(1px) translateZ(0);
    transform: perspective(1px) translateZ(0);
    box-shadow: 0 0 1px rgba(0, 0, 0, 0);
    position: relative;
    overflow: hidden;
  }

  nav .navigation button:before {
    content: "";
    position: absolute;
    z-index: -1;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    border-color: #000;
    border-style: solid;
    border-width: 0;
    -webkit-transition-property: border-width;
    transition-property: border-width;
    -webkit-transition-duration: 0.1s;
    transition-duration: 0.1s;
    -webkit-transition-timing-function: ease-out;
    transition-timing-function: ease-out;
  }

  nav .navigation button:hover:before,
  nav .navigation button:focus:before,
  nav .navigation button:active:before,
  nav .navigation button.active:before {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    border-width: 4px;
  }
</style>

<nav>
  <img class="logo" src="assets/logo.png" alt="Brawl Starts" />

  <div class="navigation">
    <button class:active={currentPage === 'home'}
      on:click={() => {
        toPage('home');
      }}>
      Home
    </button>
    <button class:active={currentPage === 'brawls'}
      on:click={() => {
        toPage('brawls');
      }}>
      Brawls
    </button>
    <button class:active={currentPage === 'details'}
      on:click={() => {
        toPage('details');
      }}>
      Detalhes
    </button>
    <button class:active={currentPage === 'contact'}
      on:click={() => {
        toPage('contact');
      }}>
      Contact
    </button>
  </div>
</nav>

{#if currentPage === 'home'}
  <Home />
{:else if currentPage === 'brawls'}
  <Brawls />
{:else if currentPage === 'details'}
  <Details />
{:else if currentPage === 'contact'}
  <Contact />
{/if}
