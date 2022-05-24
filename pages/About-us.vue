<template>
  <div class="page">
    <div class="hero__image">
      <div class="hero__text">
        <p class="company__name">SUBA CAPITAL</p>
        <p class="page__title">About Us</p>
      </div>
    </div>

    <section id="our-ideas">
      <div
        style="
          min-height: 50vh;
          position: relative;
          width: 100%;
          margin: 0px;

          background: #f1f0ea;
        "
      >
        <v-container>
          <v-row class="d-flex justify-center align-center">
            <v-col cols="12" md="5" offset-md="1">
              <div class="video-container py-16">
                <div
                  class="video__player video-frame"
                  style="background: #679436"
                ></div>
                <div class="video__player">
                  <template>
                   <lite-youtube videoid="38iML94oi_c" class="youtube-lite" />
                  </template>
                </div>
              </div>
            </v-col>
            <v-col cols="12" md="6">
              <div class="">
                <p class="sub-title">Connecting Farmers</p>
                <p class="sect__title">We are Cultivating Ideas for Growth.</p>
              </div>

              <div class="message">
                <p class="">
                  We provide leading solutions to agricultural and
                  agro-industrial production through world-class products and
                  services, always committed to meeting the needs and
                  expectations.
                </p>
                <p class="">
                  People at Suba Capital are helping farmers to emerging markets
                  maximize their profits. We use agronomic and agro-industrial
                  production through world-class products
                </p>
              </div>
            </v-col>
          </v-row>
        </v-container>
      </div>
    </section>
    <section id="our-values">
      <our-values />
    </section>
    <section id="partners">
      <partners />
    </section>
    <section id="stats" class="mb-8 mb-md-16 d-none d-lg-block">
      <stat />
    </section>
    <section>
      <testiminial />
    </section>
    <section id="our-team">
      <our-team />
    </section>
  </div>
</template>

<script>
import OurTeam from "../components/includes/our-team.vue";
import ourValues from "../components/includes/our-values.vue";
import Partners from "../components/includes/partners.vue";
import Stat from "../components/includes/stat.vue";
import Testiminial from "../components/views/testiminial.vue";

export default {
  components: { ourValues, Partners, Stat, Testiminial, OurTeam },
  name: "About",
};
</script>

<style scoped>
#our-team {
  padding-bottom: 80px;
}
.page {
  min-height: 100vh;
  width: 100%;
}
.hero__image {
  position: relative;
  height: 50vh;
  width: 100vw;
  overflow: hidden;
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("/images/pages/about/about3.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.hero__text {
  top: 50%;
  position: absolute;
  height: auto;
  width: 100%;
  background-color: #0d0d0d 65;
  text-align: center;
}
.company__name {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 33px;
  text-align: center;
  color: #ffffff;
}
.page__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 48px;
  line-height: 33px;
  color: #ffffff;
}
.sub-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #908daa;
}
.sect__title {
  font-style: normal;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: 750;
  font-size: 36px;
  line-height: 43px;
  color: #1a1544;
  max-width: 35rem;
}
.message p {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: rgba(0, 0, 0, 0.785);
}
.video__player {
  width: 100%;
  position: absolute;
  height: 300px;
  background-color: #ffffff;
  z-index: 1;
  border-radius: 25px;
}
.video-container {
  height: 400px;
  position: relative;
  /* z-index: 10; */
  justify-content: center;
  align-content: center;
}
.video-frame {
  width: 80%;
  height: 260px;
  margin-top: 80px;
  margin-left: -40px;
  border-radius: 25px;
}

.youtube-lite {
  width: 100%;
  height: 100%;
  border-radius: 25px;
}

@media only screen and (max-width: 768px) {
  .video-frame {
    display: none;
    margin: auto;
  }
  .video__player {
    border-radius: 4px;
    position: static;
  }
  .youtube-lite {
    width: 100%;
    height: 100%;
    border-radius: 4px;
  }
}
</style>
