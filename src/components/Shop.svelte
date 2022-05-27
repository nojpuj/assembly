<script>
  // Importene til ulike produkter
  import Spectrum from "./products/Spectrum.svelte";
  import KidsMiniMutt from "./products/KidsMiniMutt.svelte";
  import AnodizeGold from "./products/AnodizeGold.svelte";
  import BustOutReaper from "./products/BustOutReaper.svelte";
  import OGRipper from "./products/OGRipper.svelte";
  import FlameDot from "./products/FlameDot.svelte";
  import Kids70s from "./products/Kids70s.svelte";
  import KidsClassicDotMicro from "./products/KidsClassicDotMicro.svelte";
  import KidsVR from "./products/KidsVR.svelte";
  import LogoLand from "./products/LogoLand.svelte";
  import LevitateOrange from "./products/LevitateOrange.svelte";
  import GrenadeReaper from "./products/GrenadeReaper.svelte";
  import KidsClassic from "./products/KidsClassic.svelte";
  import PeacePurpleRed from "./products/PeacePurpleRed.svelte";
  import OdysseyLogo from "./products/OdysseyLogo.svelte";
  import OldLogo from "./products/OldLogo.svelte";

  // Setter start variabel
  let visning;

  // Funksjon til å bytte side innhold
  function sidevisning(side) {
    // Oppdaterer variabel
    visning = side;
  }
</script>

<main>
  <!-- Seksjon med id til å skrolle til -->
  <section id="Shop">
    <!-- Regulerer hva slags content som skal vises -->
    {#if visning === "Spectrum"}
      <Spectrum />
    {:else if visning === "KidsMiniMutt"}
      <KidsMiniMutt />
    {:else if visning === "AnodizeGold"}
      <AnodizeGold />
    {:else if visning === "BustOutReaper"}
      <BustOutReaper />
    {:else if visning === "OGRipper"}
      <OGRipper />
    {:else if visning === "FlameDot"}
      <FlameDot />
    {:else if visning === "Kids70s"}
      <Kids70s />
    {:else if visning === "KidsClassicDotMicro"}
      <KidsClassicDotMicro />
    {:else if visning === "KidsVR"}
      <KidsVR />
    {:else if visning === "LogoLand"}
      <LogoLand />
    {:else if visning === "LevitateOrange"}
      <LevitateOrange />
    {:else if visning === "GrenadeReaper"}
      <GrenadeReaper />
    {:else if visning === "KidsClassic"}
      <KidsClassic />
    {:else if visning === "PeacePurpleRed"}
      <PeacePurpleRed />
    {:else if visning === "OdysseyLogo"}
      <OdysseyLogo />
    {:else if visning === "OldLogo"}
      <OldLogo />
    {:else}
      <h1 class="shop-h">Shop</h1>
      <p class="shop-p">Pick your own</p>
      <div class="products">
        <!-- Bilde som man kan klikke på for å se nærmere på produktet -->
        <div class="content" on:click={() => sidevisning("Spectrum")}>
          <div class="prod-img">
            <img
              class="img"
              src="spectrum_825.jpg"
              alt="Spectrum, Black 8.25"
            />
          </div>
          <div class="prod-info">
            <h3>Alien Workshop</h3>
            <p>Spectrum, Black 8.25</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("KidsMiniMutt")}>
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
            <h3>1 499,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("AnodizeGold")}>
          <div class="prod-img">
            <img class="img" src="anodize_gold8.jpg" alt="Anodize, Gold 8.0" />
          </div>
          <div class="prod-info">
            <h3>Darkstar</h3>
            <p>Anodize, Gold 8.0</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("BustOutReaper")}>
          <div class="prod-img">
            <img
              class="img"
              src="bustoutreaper_blue7625.jpg"
              alt="Bust Out Reaper, Blue 7.625"
            />
          </div>
          <div class="prod-info">
            <h3>Blind</h3>
            <p>Bust Out Reaper, Blue 7.625</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>
      </div>

      <div class="products">
        <div class="content" on:click={() => sidevisning("OGRipper")}>
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

        <div class="content" on:click={() => sidevisning("FlameDot")}>
          <div class="prod-img">
            <img class="img" src="flamedot_825.jpg" alt="Flame Dot 8.25" />
          </div>
          <div class="prod-info">
            <h3>Santa Cruz</h3>
            <p>Flame Dot 8.25</p>
            <h3 class="price">1 399,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("Kids70s")}>
          <div class="prod-img">
            <img
              class="img"
              src="kidsseventieslogo_725.jpg"
              alt="Kids Seventies Logo 7.25"
            />
          </div>
          <div class="prod-info">
            <h3>Enjoi</h3>
            <p>Kids Seventies Logo 7.25</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div
          class="content"
          on:click={() => sidevisning("KidsClassicDotMicro")}
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

      <div class="products">
        <div class="content" on:click={() => sidevisning("KidsVR")}>
          <div class="prod-img">
            <img
              class="img"
              src="kidsvr_black725.jpg"
              alt="Kids VR, Black 7.25"
            />
          </div>
          <div class="prod-info">
            <h3>Almost</h3>
            <p>Kids VR, Black 7.25</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("LogoLand")}>
          <div class="prod-img">
            <img
              class="img"
              src="logoland_black8125.jpg"
              alt="Logo Land, Black 8.125"
            />
          </div>
          <div class="prod-info">
            <h3>Almost</h3>
            <p>Logo Land, Black 8.125</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("LevitateOrange")}>
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

        <div class="content" on:click={() => sidevisning("GrenadeReaper")}>
          <div class="prod-img">
            <img
              class="img"
              src="grenadereapercharacter_825.jpg"
              alt="Grenade Reaper Character 8.25"
            />
          </div>
          <div class="prod-info">
            <h3>Blind</h3>
            <p>Grenade Reaper Character 8.25</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>
      </div>

      <div class="products">
        <div class="content" on:click={() => sidevisning("KidsClassic")}>
          <div class="prod-img">
            <img class="img" src="kidsclassic_8.jpg" alt="Kids Classic 8.0" />
          </div>
          <div class="prod-info">
            <h3>Jart</h3>
            <p>Kids Classic 8.0</p>
            <h3 class="price">1 199,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("PeacePurpleRed")}>
          <div class="prod-img">
            <img
              class="img"
              src="peace_purplered8.jpg"
              alt="Peace Purple/Red 8.0"
            />
          </div>
          <div class="prod-info">
            <h3>Cliche</h3>
            <p>Peace Purple/Red 8.0</p>
            <h3 class="price">1 099,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("OdysseyLogo")}>
          <div class="prod-img">
            <img
              class="img"
              src="odysseylogo_825.jpg"
              alt="Odyssey Logo 8.25"
            />
          </div>
          <div class="prod-info">
            <h3>FL!P</h3>
            <p>Odyssey Logo 8.25</p>
            <h3 class="price">1 299,-</h3>
          </div>
        </div>

        <div class="content" on:click={() => sidevisning("OldLogo")}>
          <div class="prod-img">
            <img class="img" src="oldlogo_8.jpg" alt="Old Logo 8.0" />
          </div>
          <div class="prod-info">
            <h3>Cliche</h3>
            <p>Old Logo 8.0</p>
            <h3 class="price">999,-</h3>
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
    .prod-info > h3 {
      font-size: 0.5rem;
    }

    .prod-info > p {
      display: none;
    }

    .price {
      font-size: 0.4rem;
      padding: 0 0 0 0.2rem;
    }
  }
</style>
