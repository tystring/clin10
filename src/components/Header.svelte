<style>
  header {
    background-color: rgba(255, 255, 255, 0.377);
    background-image: url("/img/rpt-chevrons.png");
    background-position: center top;
    background-repeat: repeat-x;

    position: fixed;
    text-align: center;
    width: 100%;
    z-index: 1;
    top: 0;
    left: 0;
    height: 90px;
  }

  header a {
    font-weight: bold;
    color: #f63232;
    border: 4px solid #055490;
    margin-top: 20px;
    padding: 6px 12px;
    display: inline-block;
    border-radius: 36px;
    background: #ffffffb0;
    text-decoration: none;
    font-size: 1.5em;
  }

  i::before {
    color: #055490;
  }

  @media all and (max-width: 900px) {
    header {
      background-color: rgba(255, 255, 255, 0.774);
    }
  }
</style>

<header>
  <a href="/">
    <i class="fa fa-paper-plane-o" aria-hidden="true" />
    SENDFAST
  </a>
</header>
