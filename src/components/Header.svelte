<script>
</script>

<main>
  <!-- Seksjon med id til å skrolle til -->
  <section id="Home">
    <div class="header-box">
      <!-- Video uten lyd som spiller automatisk og looper seg selv når den er ferdig -->
      <video class="video" muted autoplay loop>
        <source src="skate_clip.mp4" type="video/mp4" />
        <!-- Setter undertekster til videoen om den var med lyd, dette hjelper folk med hørselsproblemer -->
        <track kind="captions" />
      </video>
      <h1 class="header">The. Best. Completes.</h1>
      <div class="header-info">
        <p>Find your dream skateboard from our selection of hardware.</p>
        <p>Discover our stores all over Oslo.</p>
      </div>
    </div>
  </section>
</main>

<style>
  .header-box {
    display: flex;
    width: 100%;
    justify-content: center;
    /* Setter alt i midten, både høyde og bredde */
    place-items: center;
  }

  .video {
    width: 100%;
    margin-top: 7.7rem;
  }

  .header {
    /* Setter teksten fritt, så jeg kan bevege det hvor jeg vil */
    position: absolute;
    font-size: 5rem;
  }

  .header-info {
    position: absolute;
    margin-top: 13rem;
    color: white;
    text-align: center;
    font-weight: 500;
  }

  /* =================== MEDIA (medium devices) =================== */

  @media screen and (max-width: 1024px) {
    .header {
      font-size: 2.5rem;
      margin-top: 6rem;
    }

    .header-info {
      font-size: 0.7rem;
      margin-top: 12rem;
    }
  }

  /* =================== MEDIA (small devices) =================== */

  @media screen and (max-width: 600px) {
    .header {
      font-size: 1.5rem;
      margin-top: 2rem;
    }

    .header-info {
      font-size: 0.5rem;
      margin-top: 7rem;
    }

    .video {
      margin-top: 3.75rem;
    }
  }
</style>
