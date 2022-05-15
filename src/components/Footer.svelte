<script>
</script>

<main>
  <footer>
    <!-- Tekst med bedrift tittel -->
    <a class="logo" href="#">Assembly</a>

    <!-- Alle linkene -->
    <ul class="permalinks">
      <!-- Ulike linker i organisert liste -->
      <li>
        <a href="#">Home</a>
      </li>
      <li>
        <a href="#NewDeals">News</a>
      </li>
      <li>
        <a href="#Locations">Parks</a>
      </li>
      <li>
        <a href="#Weather">Weather</a>
      </li>
      <li>
        <a href="#Shop">Shop</a>
      </li>
    </ul>

    <!-- Copyright tekst med unicode symbol -->
    <div class="copyright">
      <small>&copy; ASSEMBLY AS. All rights reserved</small>
    </div>
  </footer>
</main>

<style>
  footer {
    background: var(--color-p);
    padding: 3rem 0;
    text-align: center;
    font-size: 0.9rem;
    margin-top: 7rem;
  }

  /* CSS til linker */
  footer a {
    color: white;
  }

  /* Hover effekten på linkene */
  footer a:hover {
    color: var(--color-c);
  }

  .logo {
    font-size: 2rem;
    font-weight: 500;
    margin-bottom: 2rem;
    display: inline-block;
  }

  .permalinks {
    display: flex;
    justify-content: center;
    gap: 2rem;
    margin: 0 auto 3rem;
  }
</style>
