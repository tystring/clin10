<script>
  import { onMount } from "svelte";
  let code;
  let answer;

  let show = false;
  let loading = false;
  let msg;

  function chax() {
    code = "eight";
    loading = false;
  }

  function xahc() {
    loading = false;
    code = "nine";
    alert("Enter a valid Tracking");
    answer = "";
  }

  async function handleSubmit() {
    if (answer == "YM-THLK6443") {
      loading = true;
      setTimeout(chax, 2000);
    } else {
      loading = true;
      setTimeout(xahc, 2000);
    }
  }

  function handleReset() {
    code = "nine";
    answer = "";
  }
</script>

<style>
  section.join {
    background-color: #f4f4f4;
    text-align: center;
    padding: 60px 20px;
    color: #4b4b4b;
  }

  .searchbar {
    display: flex;
    justify-content: center;
    margin: 20px 0;
  }
  .searchbar input,
  .searchbar i,
  .searchbar button {
    padding: 15px 10px;
    border: none;
    background: white;
    outline: none;
  }
  .searchbar button {
    background-color: #055490;
    color: white;
    padding: 0 10px;
    transition: 0.4s;
  }
  .searchbar button:hover {
    background: green;
  }
  .searchbar input {
    width: 60%;
  }
  ol.progtrckr {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  ol.progtrckr li {
    display: inline-block;
    text-align: center;
    line-height: 3.5em;
  }

  ol.progtrckr [data-progtrckr-steps="2"] li {
    width: 49%;
  }
  ol.progtrckr [data-progtrckr-steps="4"] li {
    width: 24%;
  }
  ol.progtrckr [data-progtrckr-steps="3"] li {
    width: 33%;
  }
  ol.progtrckr [data-progtrckr-steps="5"] li {
    width: 19%;
  }
  ol.progtrckr [data-progtrckr-steps="6"] li {
    width: 16%;
  }
  ol.progtrckr [data-progtrckr-steps="7"] li {
    width: 14%;
  }
  ol.progtrckr [data-progtrckr-steps="8"] li {
    width: 12%;
  }
  ol.progtrckr [data-progtrckr-steps="9"] li {
    width: 11%;
  }

  ol.progtrckr li.progtrckr-done {
    color: black;
    border-bottom: 4px solid yellowgreen;
  }
  ol.progtrckr li.progtrckr-todo {
    color: silver;
    border-bottom: 4px solid silver;
  }

  ol.progtrckr li:after {
    content: "\00a0\00a0";
  }
  ol.progtrckr li:before {
    position: relative;
    bottom: -2.5em;
    float: left;
    left: 50%;
    line-height: 1em;
  }
  ol.progtrckr li.progtrckr-done:before {
    content: "\2713";
    color: white;
    background-color: yellowgreen;
    height: 2.2em;
    width: 2.2em;
    line-height: 2.2em;
    border: none;
    border-radius: 2.2em;
  }
  ol.progtrckr li.progtrckr-todo:before {
    content: "\039F";
    color: silver;
    background-color: white;
    font-size: 2.2em;
    bottom: -1.2em;
  }

  .but1 {
    margin-top: 58px;
    background-color: #055490;
    color: white;
    transition: 0.4s;
    padding: 15px 10px;
    border: none;
    outline: none;
  }
  .but1:hover {
    background-color: green;
  }
  .result {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .pInfo {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }

  @media all and (max-width: 900px) {
    .ol .progtrckr li {
      display: block;
      /* -webkit-box-orient: vertical;
      -webkit-box-direction: normal;
      flex-direction: column; */
    }
  }
</style>

{#if loading}
  <h2>{msg ? msg : '...searching'}</h2>
{/if}

{#if code === 'eight'}
  <div class="result">
    <h2>Track Results for shipment# {answer}</h2>
    <hr />
    <div class="pInfo">

      <div>
        <h2>Origin:</h2>
      </div>

      <div>
        <h2>Destination:</h2>
      </div>
    </div>
    <ol class="progtrckr" data-progtrckr-steps="5">
      <li class="progtrckr-done">Order Booking</li>
      <li class="progtrckr-done">Pre-Processing</li>
      <li class="progtrckr-done">In Transit</li>
      <li class="progtrckr-todo">Customs Clearing</li>
      <li class="progtrckr-todo">Delivered</li>
    </ol>
    <button class="but1" on:click={handleReset}>TRACK ANOTHER SHIPMENT</button>
  </div>
{/if}

{#if !code || code === 'nine'}
  <section class="join">
    <form class="searchbar" on:submit|preventDefault={handleSubmit}>
      <i class="fas fa-search" />
      <input
        type="search"
        bind:value={answer}
        placeholder="ENTER YOUR TRACKING" />
      <button type="submit" name="button">TRACK SHIPMENT</button>
    </form>
  </section>
{/if}
