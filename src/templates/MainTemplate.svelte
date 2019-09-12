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
    ul {
        display: flex;
        justify-content: space-around;
        align-items: center;
        list-style: none;
    }
</style>

<ul>
    <li><button on:click={()=>{ toPage('home') }} >Home</button></li>
    <li><button on:click={()=>{ toPage('brawls') }} >Brawls</button></li>
    <li><button on:click={()=>{ toPage('details') }} >Detalhes</button></li>
    <li><button on:click={()=>{ toPage('contact') }} >Contact</button></li>
</ul>

{#if currentPage === 'home'}
  <Home />
{:else if currentPage === 'brawls'}
  <Brawls />
{:else if currentPage === 'details'}
  <Details />
{:else if currentPage === 'contact'}
  <Contact />
{/if}
