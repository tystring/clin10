<script>
  //import Banner from "../components/Banner.svelte";
  //import Carousel from '../components/Carousel.svelte'
  import TransitionWrapper from "../components/TransitionWrapper.svelte";
</script>

<style>
  main {
    max-width: 100%;
    width: 1200px;
    margin: 80px auto;
    padding: 0 40px;
    box-sizing: border-box;
    height: 100%;
    font-family: "Montserrat", sans-serif;
  }

  a {
    text-decoration: none;
    margin: 1rem 0;
    font-weight: 600;
    text-transform: uppercase;
    font-size: 0.8125rem;
    letter-spacing: 1px;
  }

  p {
    font-size: 0.9rem;
    margin: 1rem 0;
    line-height: 1.5;
  }

  .service a {
    color: #5b7abb;
    display: block;
  }

  .service h4 {
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    color: #56ceba;
    font-size: 1.3rem;
    margin: 1rem 0 0.6rem;
  }

  .services-grid {
    display: -webkit-box;
    display: flex;
    -webkit-box-align: center;
    align-items: center;
  }

  .service {
    background: #fff;
    margin: 20px;
    padding: 20px;
    border-radius: 4px;
    text-align: center;
    -webkit-box-flex: 1;
    flex: 1;
    display: -webkit-box;
    display: flex;
    flex-wrap: wrap;
    border: 2px solid #e7e7e7;
    -webkit-transition: all 0.3s ease;
    -moz-transition: all 0.3s ease;
    transition: all 0.3s ease;
  }

  .service:hover {
    -webkit-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.08);
    -moz-box-shadow: 0 5px 10px rgba(0, 0, 0, 0.08);
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.08);
  }

  .service i {
    font-size: 3.45rem;
    margin: 1rem 0;
  }

  .service1 i,
  .service1 h4,
  .service1 .cta {
    color: #42b7ca;
  }

  .service1:hover {
    border: 2px solid #42b7ca;
  }

  .service2 i,
  .service2 h4,
  .service2 .cta {
    color: #425fca;
  }

  .service2:hover {
    border: 2px solid #425fca;
  }

  .service3 i,
  .service3 h4,
  .service3 .cta {
    color: #9c42ca;
  }

  .service3:hover {
    border: 2px solid #9c42ca;
  }

  .service .cta span {
    font-size: 0.6rem;
  }

  .service > * {
    flex: 1 1 100%;
  }

  .service .cta {
    align-self: flex-end;
  }

  @media all and (max-width: 900px) {
    .services-grid {
      display: -webkit-box;
      display: flex;
      -webkit-box-orient: vertical;
      -webkit-box-direction: normal;
      flex-direction: column;
    }
  }
</style>

<svelte:head>
  <title>SendFast Logistics and Courier</title>
</svelte:head>

<TransitionWrapper>
  <main>
    <div class="services-grid">
      <div class="service service1">
        <i class="one fas fa-3x fa-shipping-fast" />
        <h4>Express Delivery Services</h4>
        <p>
          Use our world-class leading proprietary tool to search rates based on
          the vessel schedules and your commodity.
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>

      <div class="service service2">
        <i class="fas fa-plane-departure fa-3x" />
        <h4>International Courier Services</h4>
        <p>
          Use our class leading proprietary tool to search rates based on the
          vessel schedules and your commodity.
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>

      <div class="service service3">
        <i class="fas fa-user-shield fa-3x" />
        <h4>Safer and Secure Deliveries</h4>
        <p>
          Use our class leading proprietary tool to search rates based on the
          vessel schedules and your commodity.
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>
    </div>

  </main>
</TransitionWrapper>
