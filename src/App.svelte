<script>
  // Importerer komponentene
  import Header from "./components/Header.svelte";
  import Nav from "./components/Nav.svelte";
  import NewDeals from "./components/NewDeals.svelte";
  import Locations from "./components/Locations.svelte";
  import Weather from "./components/Weather.svelte";
  import Shop from "./components/Shop.svelte";
  import Footer from "./components/Footer.svelte";
</script>

<main>
  <!-- Viser alle på siden, i riktig rekkefølge -->
  <Nav />
  <Header />
  <NewDeals />
  <Locations />
  <Weather />
  <Shop />
  <Footer />
</main>

<style>
</style>
