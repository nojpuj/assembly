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
          src="grenadereapercharacter_825.jpg"
          alt="Grenade Reaper Character 8.25"
        />
      </div>
      <div class="prod-info">
        <h1 class="header">Blind</h1>
        <p class="info">Grenade Reaper Character 8.25</p>
        <h3 class="price">1 299,-</h3>
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
    background-color: var(--color-c);
    border-radius: 2rem;
    left: 2rem;
    top: 2rem;
  }

  .img {
    width: 20rem;
    border-radius: 2rem;
  }
</style>
