<template>
  <div>
    <section class="hero is-fullheight is-white">
      <div class="hero-body">
        <div
          id="title-and-buttons-container"
          class="container"
        >
          <div class="columns">
            <div class="column">
              <span
                id="maintitle"
                class="is-size-3-mobile"
              >
                konfluence <span id="yearnumber">
                  2019
                </span>
              </span>
              <h2 class="subtitle is-size-4-desktop is-size-5-mobile">
                First of its kind student-organized front-end conference |
                <span class="date">
                  April 26th
                </span>
              </h2>
            </div>
          </div>
          <div
            class="button-row level"
            :class="this.isMobile() ? 'increased-top-margin' : ''"
          >
            <div class="columns level-left">
              <div class="column">
                <a
                  v-scroll-to="'#tickets'"
                  class="button is-primary is-outlined is-large is-rounded"
                  :class="this.isMobile() ? 'is-fullwidth' : ''"
                >
                  TICKETS
                </a>
              </div>
              <div class="column">
                <a
                  v-scroll-to="'#speakers'"
                  title="Speakers"
                  class="button is-success is-outlined is-large is-rounded"
                  :class="this.isMobile() ? 'is-fullwidth' : ''"
                >
                  SPEAKERS
                </a>
              </div>
              <div class="column">
                <a
                  v-scroll-to="'#agenda'"
                  title="Agenda"
                  class="button is-primary is-outlined is-large is-rounded"
                  :class="this.isMobile() ? 'is-fullwidth' : ''"
                >
                  AGENDA
                </a>
              </div>
              <div class="column">
                <a
                  v-scroll-to="'#organizers'"
                  class="button is-info is-outlined is-large is-rounded"
                  :class="this.isMobile() ? 'is-fullwidth' : ''"
                >
                  CONTACT
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="hero is-medium gradient">
      <div class="hero-body" />
    </section>
  </div>
</template>

<script>
export default {
  name: "Launch",
  mounted() {
    const ticketScript = document.createElement('script');
    ticketScript.setAttribute('src', 'https://fienta.com/embed.js');
    document.head.appendChild(ticketScript);
  },
  methods: {
    isMobile: function () {
      return screen.width < 900;
    }
  }
}
</script>

<style scoped>
  @font-face {
    font-family: "Keep Calm";
    src: url(../assets/fonts/KeepCalm-Medium.ttf) format('truetype')
  }

  .hero {
    text-align: left;
    z-index: 10;
  }

  .gradient {
    background-image: linear-gradient(white, #f7f7f7)
  }

  .button-row {
    margin-top: 30px;
  }

  @media (max-width: 900px) {
    .button-row {

    }
  }

  #maintitle {
    font-family: "Keep Calm", sans-serif;
    font-weight: 500;
    font-size: 60pt;
    /*white-space: nowrap;*/
  }

  #yearnumber {
    color: #3498db;
  }

  #title-and-buttons-container {
    z-index: 30;
  }

  .increased-top-margin {
    margin-top: 80px;
  }

  .date {
    /*padding-bottom: 1rem;*/
    color: #1ed385;
    font-weight: 700;
  }
</style>