<script>
  // Importene til ulike produkter
  import OGRipperNew from "./products/OGRipperNew.svelte";
  import KidsMiniMuttNew from "./products/KidsMiniMuttNew.svelte";
  import LevitateOrangeNew from "./products/LevitateOrangeNew.svelte";
  import KidsClassicDotMicroNew from "./products/KidsClassicDotMicroNew.svelte";

  // Setter start variabel
  let visning;

  // Funksjon til å bytte side content
  function sidevisning(side) {
    // Oppdaterer variabel
    visning = side;
  }
</script>

<main>
  <!-- Seksjon med id til å skrolle til -->
  <section id="NewDeals">
    <!-- Regulerer hva slags content som skal vises -->
    {#if visning === "OGRipperNew"}
      <OGRipperNew />
    {:else if visning === "KidsMiniMuttNew"}
      <KidsMiniMuttNew />
    {:else if visning === "LevitateOrangeNew"}
      <LevitateOrangeNew />
    {:else if visning === "KidsClassicDotMicroNew"}
      <KidsClassicDotMicroNew />
    {:else}
      <h1>New Releases</h1>
      <p>The freshiest heat</p>
      <div class="products">
        <!-- Bilde som man kan klikke på for å se nærmere på produktet -->
        <div class="content" on:click={() => sidevisning("OGRipperNew")}>
          <div class="prod-img">
            <img
              class="img"
              src="ogripper_red775.jpg"
              alt="OG Ripper, Red/Orange 7.75"
            />
          </div>
          <div class="prod-info">
            <h3>Blind</h3>
            <p>OG Ripper, Red/Orange 7.75</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("KidsMiniMuttNew")}>
          <div class="prod-img">
            <img
              class="img"
              src="kidsminintt_7375.jpg"
              alt="Kids Mini Mutt 7.375"
            />
          </div>
          <div class="prod-info">
            <h3>Almost</h3>
            <p>Kids Mini Mutt 7.375</p>
            <h3 class="price">1 499,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("LevitateOrangeNew")}>
          <div class="prod-img">
            <img
              class="img"
              src="levitate_orange8.jpg"
              alt="Levitate, Orange 8.0"
            />
          </div>
          <div class="prod-info">
            <h3>Darkstar</h3>
            <p>Levitate, Orange 8.0</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div
          class="content"
          on:click={() => sidevisning("KidsClassicDotMicroNew")}
        >
          <div class="prod-img">
            <img
              class="img"
              src="kidsclassicdotmicro_75.jpg"
              alt="Kids Classic Dot Micro 7.5"
            />
          </div>
          <div class="prod-info">
            <h3>Santa Cruz</h3>
            <p>Kids Classic Dot Micro 7.5</p>
            <h3 class="price">1 499,-</h3>
          </div>
        </div>
      </div>
    {/if}
  </section>
</main>

<style>
  .products {
    display: flex;
    flex-direction: row;
    background: transparent;
    text-align: left;
    gap: 0.5rem;
    padding: 0.5rem 0.5rem 0 0.5rem;
  }

  .content {
    cursor: pointer;
  }

  .prod-info {
    padding: 0.2rem 0 0 0.2rem;
  }

  .img {
    width: 100%;
  }

  /* =================== MEDIA (medium devices) =================== */

  @media screen and (max-width: 1024px) {
    .prod-info > h3 {
      font-size: 0.9rem;
    }

    .prod-info > p {
      font-size: 0.55rem;
    }
  }

  /* =================== MEDIA (small devices) =================== */

  @media screen and (max-width: 600px) {
    .prod-info > p {
      display: none;
    }

    .price {
      font-size: 0.7rem;
      padding: 0 0 0 0.2rem;
    }
  }
</style>
