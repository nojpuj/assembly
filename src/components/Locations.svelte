<script>
</script>

<main>
  <!-- Seksjon med id til å skrolle til -->
  <section id="Locations">
    <h1>Park Locations</h1>
    <p>Where to « send it »</p>
    <div class="maps">
      <!-- iframe tatt fra google maps api siden -->
      <iframe
        width="100%"
        height="720px"
        id="gmap_canvas"
        src="https://maps.google.com/maps?q=skatepark=&output=embed"
        frameborder="0"
        scrolling="no"
        marginheight="0"
        marginwidth="0"
        title="maps"
      />
    </div>
  </section>
</main>

<style>
  .maps {
    display: flex;
    justify-content: center;
    padding: 0.5rem 0.5rem 0 0.5rem;
  }
</style>
