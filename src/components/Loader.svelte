<script>
  import { onMount } from "svelte";
  let name = "world";
  let show = false;
  let waiting = false;

  function chax() {
    waiting = false;
    return (show = true);
  }
  onMount(() => {
    waiting = true;
    setTimeout(chax, 2000);
  });
</script>

{#if waiting}
  <p>...loading</p>
{/if}

{#if show}
  <h1>Hello {name}!</h1>
{/if}
