<script>
</script>

<main>
  <nav>
    <!-- Ulike linker med # href for å skrolle til de ulike seksjonene -->
    <div class="menu-wrap">
      <input type="checkbox" class="toggler" />
      <div class="hamburger">
        <div />
      </div>
      <div class="menu">
        <div>
          <div>
            <a class="link-h" href="#">Home</a>
            <a class="links" href="#NewDeals">News</a>
            <a class="links" href="#Locations">Parks</a>
            <a class="logo" href="#">
              <img src="logo.png" alt="logo" class="logo-img" />
            </a>
            <a class="links" href="#Weather">Weather</a>
            <a class="links" href="#Shop">Shop</a>
          </div>
        </div>
      </div>
    </div>
  </nav>
</main>

<style>
  nav {
    top: 0;
    position: fixed;
    display: flex;
    justify-content: center;
    width: 100%;
    z-index: 2;
    gap: 0.8rem;
    background: var(--color-bg);
  }

  .menu-wrap .menu > div > div {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    margin-bottom: 2rem;
    gap: 1.2rem;
  }

  .links {
    display: flex;
    justify-content: center;
    padding: 0.9rem;
    display: flex;
    color: white;
    font-size: 1.1rem;
  }

  .link-h {
    position: absolute;
    visibility: hidden;
    display: flex;
    justify-content: center;
    padding: 0.9rem;
    display: flex;
    color: white;
    font-size: 1.1rem;
  }

  nav a:hover {
    color: var(--color-c);
  }

  .logo-img {
    width: 4rem;
  }

  .menu-wrap .toggler {
    opacity: 0;
  }

  /* =================== MEDIA (small devices) =================== */

  @media screen and (max-width: 600px) {
    .menu-wrap {
      position: fixed;
      top: 0;
      left: 0;
      z-index: 1;
      display: flex;
      justify-content: center;
      width: 100%;
    }

    .menu-wrap .toggler {
      position: absolute;
      top: 0;
      left: 0;
      z-index: 2;
      cursor: pointer;
      width: 50px;
      height: 50px;
      opacity: 0;
    }

    .menu-wrap .hamburger {
      position: absolute;
      top: 0;
      left: 0;
      z-index: 1;
      width: 100%;
      height: 60px;
      padding: 1rem;
      background: var(--color-bg);
      display: flex;
      align-items: center;
    }

    .menu-wrap .hamburger > div {
      position: relative;
      width: 30px;
      height: 2px;
      background: white;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: var(--transition);
    }

    .menu-wrap .hamburger > div:before,
    .menu-wrap .hamburger > div:after {
      content: "";
      position: absolute;
      z-index: 1;
      top: -10px;
      width: 100%;
      height: 2px;
      background: inherit;
    }

    .menu-wrap .hamburger > div:after {
      top: 10px;
    }

    .menu-wrap .toggler:checked + .hamburger > div {
      transform: rotate(135deg);
    }

    .menu-wrap .toggler:checked + .hamburger > div:before,
    .menu-wrap .toggler:checked + .hamburger > div:after {
      top: 0;
      transform: rotate(90deg);
    }

    .menu-wrap .toggler:checked:hover + .hamburger > div {
      transform: rotate(225deg);
    }

    /* Show menu */
    .menu-wrap .toggler:checked ~ .menu {
      visibility: visible;
    }

    .menu-wrap .toggler:checked ~ .menu > div {
      transform: scale(1);
      transition-duration: all 0.5s ease;
    }

    .menu-wrap .toggler:checked ~ .menu > div > div {
      opacity: 1;
      transition: opacity 0.4s ease;
    }

    .menu-wrap .menu {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      visibility: hidden;
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .menu-wrap .menu > div {
      background: rgba(24, 39, 51, 0.85);
      width: 100%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
      transform: scale(0);
      transition: var(--transition);
    }

    .menu-wrap .menu > div > div {
      text-align: center;
      max-width: 90vw;
      max-height: 100vh;
      opacity: 0;
      transition: opacity 0.4s ease;
      flex-direction: column;
    }

    .menu-wrap .menu > div > div > a {
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
      padding: 0.7rem;
    }

    .logo {
      position: absolute;
      visibility: hidden;
    }

    .link-h {
      position: relative;
      visibility: visible;
    }
  }
</style>
