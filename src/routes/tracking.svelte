<script>
  import Track from "../components/Track.svelte";
  import TransitionWrapper from "../components/TransitionWrapper.svelte";
</script>

<style>
  h2,
  p {
    font-family: "Montserrat", sans-serif;
  }
</style>

<svelte:head>
  <title>Shipment Tracking</title>
</svelte:head>

<TransitionWrapper>
  <h2>Shipment Tracking</h2>

  <p>
    Providing cargo service to 127 countries worldwide, SendFast’s New
    artificial intelligence robot provides you with the opportunity to inquire
    the status of your cargo 24/7. You can at any time inquire the status of all
    of your cargo shipments and check for the flights that meet your
    requirements.
  </p>
  <Track />
</TransitionWrapper>
