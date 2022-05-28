<script>
  // Lager start variabler
  let date_now;
  let icon_now;
  let cmt_now;
  let temp_now;
  let wind_now;

  let day0_icon;
  let day0_day;
  let day0_cmt;
  let day0_max;
  let day0_min;

  let day1_icon;
  let day1_day;
  let day1_cmt;
  let day1_max;
  let day1_min;

  let day2_icon;
  let day2_day;
  let day2_cmt;
  let day2_max;
  let day2_min;

  let day3_icon;
  let day3_day;
  let day3_cmt;
  let day3_max;
  let day3_min;

  // Definerer laster variabel
  let loading;

  // Henter api med funksjon
  let weather = async () => {
    // Oppdateter variabel før
    loading = false;

    let data = await fetch(
      `https://weatherdbi.herokuapp.com/data/weather/oslo`
    );

    let json = await data.json();

    // Oppdaterer variablene
    // Nå
    date_now = json.currentConditions.dayhour;
    icon_now = json.currentConditions.iconURL;
    cmt_now = json.currentConditions.comment;
    temp_now = json.currentConditions.temp.c;
    wind_now = json.currentConditions.wind.km;

    // Dag 2
    day0_icon = json.next_days[1].iconURL;
    day0_day = json.next_days[1].day;
    day0_cmt = json.next_days[1].comment;
    day0_max = json.next_days[1].max_temp.c;
    day0_min = json.next_days[1].min_temp.c;

    // Dag 3
    day1_icon = json.next_days[2].iconURL;
    day1_day = json.next_days[2].day;
    day1_cmt = json.next_days[2].comment;
    day1_max = json.next_days[2].max_temp.c;
    day1_min = json.next_days[2].min_temp.c;

    // Dag 4
    day2_icon = json.next_days[3].iconURL;
    day2_day = json.next_days[3].day;
    day2_cmt = json.next_days[3].comment;
    day2_max = json.next_days[3].max_temp.c;
    day2_min = json.next_days[3].min_temp.c;

    // Dag 5
    day3_icon = json.next_days[4].iconURL;
    day3_day = json.next_days[4].day;
    day3_cmt = json.next_days[4].comment;
    day3_max = json.next_days[4].max_temp.c;
    day3_min = json.next_days[4].min_temp.c;

    // Oppdateter variabel etter
    loading = true;
  };

  // kjører fuksjonen
  weather();
</script>

<main>
  <!-- Seksjon med id til å skrolle til -->
  <section id="Weather">
    <h1 class="header">Weather in Oslo</h1>
    <p class="header-p">Is it time to skate?</p>
    <!-- Hele vær-widgeten, altså hele komponentet -->
    <div class="widget">
      <!-- If-løkke som kontrollerer om komponentet laster eller har lasta -->
      <!-- {#if loading} -->
      <!-- Egen kolonne til hver dag -->
      <div class="lane">
        <!-- Setter inn oppdaterte variabler -->
        <h1>{date_now}</h1>
        <!-- Første er annerldedes (lane2) fordi boksen skal være bredere -->
        <div class="lane2">
          <!-- Bilde/icon -->
          <div class="icon">
            <img src={icon_now} alt="icon" class="icon" />
            <!-- Tilstander i tekst -->
            <h2 class="temp-now">{temp_now} &#176;C</h2>
            <p>{cmt_now}</p>
          </div>
          <div class="conditions">
            <!-- Temperatur -->
            <!-- Bruker grader unicode som grader-tegnet -->
            <h2>{temp_now} &#176;C</h2>
            <!-- Vind, med unicode symbol -->
            <!-- Regner om km/t til m/s -->
            <p>&#128168; {(wind_now / 3.6).toFixed(1)} m/s</p>
          </div>
        </div>
      </div>
      <div class="lane">
        <h1>{day0_day}</h1>
        <div class="info">
          <img src={day0_icon} alt="icon" class="icon" />
          <p>{day0_cmt}</p>
          <p class="temp-high">{day0_max} &#176;C</p>
          <p class="temp-low">{day0_min} &#176;C</p>
        </div>
      </div>
      <div class="lane">
        <h1>{day1_day}</h1>
        <div class="info">
          <img src={day1_icon} alt="icon" class="icon" />
          <p>{day1_cmt}</p>
          <p class="temp-high">{day1_max} &#176;C</p>
          <p class="temp-low">{day1_min} &#176;C</p>
        </div>
      </div>
      <div class="lane">
        <h1>{day2_day}</h1>
        <div class="info">
          <img src={day2_icon} alt="icon" class="icon" />
          <p>{day2_cmt}</p>
          <p class="temp-high">{day2_max} &#176;C</p>
          <p class="temp-low">{day2_min} &#176;C</p>
        </div>
      </div>
      <div class="lane">
        <h1>{day3_day}</h1>
        <div class="info">
          <img src={day3_icon} alt="icon" class="icon" />
          <p>{day3_cmt}</p>
          <p class="temp-high">{day3_max} &#176;C</p>
          <p class="temp-low">{day3_min} &#176;C</p>
        </div>
      </div>
      <!-- {:else} -->
      <!-- Tekst om api fortsatt loader -->
      <!-- <p class="loading">Loading...</p> -->
      <!-- {/if} -->
    </div>
  </section>
</main>

<style>
  .header {
    font-size: 3rem;
  }

  .header-p {
    font-size: 1rem;
  }

  h1 {
    font-size: 1.2rem;
  }

  h2 {
    font-size: 0.8rem;
  }

  p {
    font-size: 0.7rem;
  }

  .widget {
    display: flex;
    flex-direction: row;
    justify-content: center;
    place-items: center;
    width: 100%;
  }

  .lane {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    padding: 1.5rem;
    text-align: center;
  }

  .conditions {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .lane2 {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: row;
    gap: 0.9rem;
  }

  .icon {
    width: 8rem;
  }

  .temp-high {
    color: red;
  }

  .temp-low {
    color: lightskyblue;
  }

  .temp-now {
    position: absolute;
    visibility: hidden;
  }

  .loading {
    text-align: center;
    font-size: 1.4rem;
  }

  /* =================== MEDIA (medium devices) =================== */

  @media screen and (max-width: 1024px) {
    .header {
      font-size: 2.5rem;
    }

    .header-p {
      font-size: 0.7rem;
    }

    h1 {
      font-size: 0.9rem;
    }

    h2 {
      font-size: 0.49rem;
    }

    p {
      font-size: 0.4rem;
    }

    .loading {
      text-align: center;
      font-size: 1rem;
    }

    .icon {
      width: 4rem;
    }

    .lane {
      padding: 1rem;
    }

    .lane2 {
      gap: 0.4rem;
    }
  }

  /* =================== MEDIA (small devices) =================== */

  @media screen and (max-width: 600px) {
    .header {
      font-size: 1.5rem;
    }

    .header-p {
      font-size: 0.5rem;
    }

    h1 {
      font-size: 0.6rem;
    }

    h2 {
      font-size: 0.45rem;
    }

    p {
      font-size: 0.35rem;
    }

    .loading {
      text-align: center;
      font-size: 0.6rem;
    }

    .icon {
      width: 3.2rem;
    }

    .lane {
      padding: 0.8rem;
    }

    .lane2 {
      gap: 0.5rem;
      flex-direction: column;
    }

    .conditions {
      position: absolute;
      visibility: hidden;
    }

    .temp-now {
      position: relative;
      visibility: visible;
    }
  }
</style>
