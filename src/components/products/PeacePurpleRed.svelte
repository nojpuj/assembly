<script>
  import Shop from "../Shop.svelte";

  let visning;

  function sidevisning(side) {
    visning = side;
  }
</script>

<main>
  {#if visning === "Shop"}
    <Shop />
  {:else}
    <h1 class="shop-h">Shop</h1>
    <p class="shop-p">Pick your own</p>
    <div class="content">
      <div class="prod-img">
        <img
          class="img"
          src="peace_purplered8.jpg"
          alt="Peace Purple/Red 8.0"
        />
      </div>
      <div class="prod-info">
        <h1 class="header">Cliche</h1>
        <p class="info">Peace Purple/Red 8.0</p>
        <h3 class="price">1 099,-</h3>
        <br />
        <button class="btn" on:click={() => sidevisning("Shop")}
          >Back to Shop</button
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
    border-radius: 2rem;
    left: 2rem;
    top: 2rem;
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
      margin-left: 2rem;
    }

    .header {
      font-size: 1.1rem;
    }

    .info {
      font-size: 0.7rem;
    }

    .price {
      font-size: 1rem;
    }

    .img {
      width: 10rem;
      border-radius: 2rem;
    }
  }
</style>
