<script>
  import Carousel from "@beyonk/svelte-carousel";
  import { ChevronLeftIcon, ChevronRightIcon } from "svelte-feather-icons";
  import { fade, slide, scale } from "svelte/transition";
</script>

<style>
  .slide-content {
    position: relative;
    width: 100%;
    height: 600px;
    min-height: 400px;
  }

  img {
    width: 100%;
    max-width: 100%;
    max-height: 100%;
    object-fit: cover;
    display: block;
  }
  .control :global(svg) {
    width: 100%;
    height: 100%;
    color: #fff;
    border: 2px solid #fff;
    border-radius: 32px;
  }

  @media screen and (max-width: 600px) {
    .slide-content {
      display: flex;
      width: 100%;
      vertical-align: top;
    }
  }
</style>

<Carousel perPage={1} loop autoplay={5999}>
  <span class="control" slot="left-control">
    <ChevronLeftIcon />
  </span>

  <div class="slide-content">
    <img src="img/sss.jpg" alt="Kitten 1" />

  </div>

  <div class="slide-content">
    <img src="img/aa.jpg" alt="Kitten 1" />
  </div>

  <div class="slide-content">
    <img src="img/Carg.jpg" alt="Kitten 1" />
  </div>

  <span class="control" slot="right-control">
    <ChevronRightIcon />
  </span>
</Carousel>
