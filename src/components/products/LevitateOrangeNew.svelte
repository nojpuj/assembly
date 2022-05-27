<script>
  import NewDeals from "../NewDeals.svelte";

  let visning;

  function sidevisning(side) {
    visning = side;
  }
</script>

<main>
  {#if visning === "NewDeals"}
    <NewDeals />
  {:else}
    <h1 class="shop-h">New Releases</h1>
    <p class="shop-p">The freshiest heat</p>
    <div class="content">
      <div class="prod-img">
        <img
          class="img"
          src="levitate_orange8.jpg"
          alt="Levitate, Orange 8.0"
        />
      </div>
      <div class="prod-info">
        <h1 class="header">Darkstar</h1>
        <p class="info">Levitate, Orange 8.0</p>
        <h3 class="price">1 299,-</h3>
        <br />
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
      margin-left: 2rem;
      width: 10rem;
      border-radius: 2rem;
    }

    .btn {
      width: 75%;
    }
  }
</style>
