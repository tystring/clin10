<script>
  import TransitionWrapper from "../components/TransitionWrapper.svelte";
</script>

<style>
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

  section {
    max-width: 1000px;
    margin: 0 auto;
    text-align: center;
    padding: 30px;
  }

  h3 {
    font-family: "Montserrat", sans-serif;
    font-weight: 600;
    color: #333;
    font-size: 1.825rem;
    margin: 1.3rem 0;
  }

  .section-lead {
    max-width: 600px;
    margin: 1rem auto 1.5rem;
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

<TransitionWrapper>
  <section>
    <h3>Our Services</h3>
    <p class="section-lead">
      Your cargoes are carefully handled in SendFast’s technological warehouse
      with the help of its dedicated workforce in Istanbul, which is a natural
      HUB thanks to its characteristic of being the crossroads of continents
      throughout history. Your cargoes can be delivered directly to 127
      countries in the world with the wide network and fleet power of SendFast
      partner Airlines.
    </p>
    <div class="services-grid">
      <div class="service service1">
        <i class="fab fa-usps" />
        <h4>Special Cargo</h4>
        <p>
          SendFast delivers all kinds of cargo from small packages to valuable
          items, spare parts and technological products under suitable
          conditions.
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>

      <div class="service service2">
        <i class="fas fa-map-marker-alt" />
        <h4>Station Information</h4>
        <p>
          Find the nearest SendFast Location from our numerous service outlets,
          strategically located to bring quality delivery closer to your
          doorstep .
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>

      <div class="service service3">
        <i class="fas fa-plane-slash" />
        <h4>Charter</h4>
        <p>
          Cargo charter flights are special for the purpose of renting of the
          entire capacity of an aircraft by any cargo customer.
        </p>
        <a href="contact" class="cta">
          Contact Us
          <span class="ti-angle-right" />
        </a>
      </div>
    </div>
  </section>
</TransitionWrapper>
