<script>
</script>

<main>
  <nav>
    <!-- Ulike linker med # href for å skrolle til de ulike seksjonene -->
    <a href="#NewDeals">News</a>
    <a href="#Locations">Parks</a>
    <a class="logo" href="#">
      <img src="logo.png" alt="logo" class="logo-header" />
    </a>
    <a href="#Weather">Weather</a>
    <a href="#Shop">Shop</a>
  </nav>
</main>

<style>
  nav {
    position: fixed;
    display: flex;
    justify-content: center;
    width: 100%;
    z-index: 2;
    gap: 0.8rem;
    background: var(--color-bg);
  }

  nav a {
    padding: 0.9rem;
    display: flex;
    color: white;
    font-size: 1.1rem;
    place-items: center;
  }

  nav a:hover {
    color: var(--color-c);
  }

  .logo {
    width: 8rem;
  }
</style>
