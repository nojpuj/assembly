<script>
  // Importerer nyeste utgaver for å bytte visning til
  import NewDeals from "../NewDeals.svelte";

  let visning;

  function sidevisning(side) {
    visning = side;
  }
</script>

<main>
  <!-- Kontrollerer visningen -->
  {#if visning === "NewDeals"}
    <NewDeals />
  {:else}
    <h1 class="shop-h">New Releases</h1>
    <p class="shop-p">The freshiest heat</p>
    <div class="content">
      <div class="prod-img">
        <img
          class="img"
          src="kidsclassicdotmicro_75.jpg"
          alt="Kids Classic Dot Micro 7.5"
        />
      </div>
      <div class="prod-info">
        <h1 class="header">Santa Cruz</h1>
        <p class="info">Kids Classic Dot Micro 7.5</p>
        <h3 class="price">1 499,-</h3>
        <br />
        <!-- Knapp til å bytte tilbake til NewDeals -->
        <button class="btn" on:click={() => sidevisning("NewDeals")}
          >Back to New Releases</button
        >
      </div>
    </div>
  {/if}
</main>

<style>
  .content {
    display: flex;
    flex-direction: row;
    justify-content: center;
  }

  .prod-info {
    display: flex;
    justify-content: center;
    flex-direction: column;
    margin-left: 5rem;
  }

  .header {
    font-size: 3rem;
  }

  .info {
    font-size: 1.5rem;
  }

  .price {
    font-size: 2rem;
  }

  .prod-img {
    background-color: var(--color-c);
    border-radius: 2rem;
  }

  .img {
    width: 20rem;
    border-radius: 2rem;
  }

  /* =================== MEDIA (medium devices) =================== */

  @media screen and (max-width: 1024px) {
    .prod-info {
      margin-left: 4rem;
    }

    .header {
      font-size: 2rem;
    }

    .info {
      font-size: 1rem;
    }

    .price {
      font-size: 1.3rem;
    }

    .img {
      width: 15rem;
      border-radius: 2rem;
    }
  }

  /* =================== MEDIA (small devices) =================== */

  @media screen and (max-width: 600px) {
    .prod-info {
      margin-left: 3rem;
    }

    .header {
      font-size: 1.5rem;
    }

    .info {
      font-size: 0.7rem;
    }

    .price {
      font-size: 1rem;
    }

    .img {
      width: 12rem;
      border-radius: 2rem;
    }

    .btn {
      width: 75%;
    }
  }
</style>
