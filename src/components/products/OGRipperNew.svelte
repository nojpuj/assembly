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
          src="ogripper_red775.jpg"
          alt="OG Ripper, Red/Orange 7.75"
        />
      </div>
      <div class="prod-info">
        <h1 class="header">Blind</h1>
        <p class="info">OG Ripper, Red/Orange 7.75</p>
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
