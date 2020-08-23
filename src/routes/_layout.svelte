<script>
  import Nav from "../components/Nav.svelte";
  import Footer from "../components/Footer.svelte";
  import Prefooter from "../components/Prefooter.svelte";
  import Header from "../components/Header.svelte";
  import Banner from "../components/Banner.svelte";
  export let segment;
</script>

<style>
  main {
    position: relative;
    max-width: 76em;
    background-color: white;
    padding: 2em;
    margin: 0 auto;
    box-sizing: border-box;
  }
</style>

{#if segment === undefined}
  <Header />
  <Banner />

  <Nav {segment} />
  <main>
    <slot />
  </main>
  <Prefooter />
  <Footer />
{:else}
  <Header />
  <Nav {segment} />
  <main style="margin-top:86px; height: 60vh;">

    <slot />
  </main>
  <Prefooter />
  <Footer />
{/if}
