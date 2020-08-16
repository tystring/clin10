<script>
  export let segment;

  export let active = false;

  function toggle() {
    if (active) {
      active = false;
    } else {
      active = true;
    }
  }
</script>

<style>
  nav {
    background-color: #f4f4f4;
    padding: 20px;
    position: sticky;
    top: 83px;
    z-index: 3;
  }

  nav ul {
    max-width: 1200px;
    white-space: nowrap;
    margin: 0 auto;
  }

  nav li {
    width: 25%;
    display: inline-block;
  }

  nav li a {
    text-decoration: none;
    color: #484b4b;
  }

  nav li a.join {
    color: #f63232;
    font-weight: bold;
  }

  nav li a.active {
    font-weight: bold;
    text-align: left;
  }

  nav li :hover {
    border-bottom: 2px solid #f63232;
  }

  .icon {
    display: none;
  }

  @media screen and (max-width: 600px) {
    .icon {
      color: #f63232;
      display: block;
    }

    nav li a.join {
      display: none;
    }

    nav li {
      width: 25%;
      display: block;
    }
  }
</style>

<nav class="main-nav">
  <ul>
    <li>
      <a
        aria-current={segment === undefined ? 'page' : undefined}
        href="."
        class={active ? 'active' : 'join'}>
        Home
      </a>
    </li>
    <li>
      <a
        aria-current={segment === '' ? 'page' : undefined}
        href="tracking"
        class={active ? 'active' : 'join'}>
        Track Shipment
      </a>
    </li>
    <li>
      <a
        aria-current={segment === '' ? 'page' : undefined}
        href="services"
        class={active ? 'active' : 'join'}>
        Services
      </a>
    </li>

    <li>
      <a
        aria-current={segment === '' ? 'page' : undefined}
        href="contact"
        class={active ? 'active' : 'join'}>
        Contact
      </a>
    </li>

    <a on:click={toggle} href="." class="icon">
      <i class="fa fa-bars" />
    </a>
  </ul>

</nav>
