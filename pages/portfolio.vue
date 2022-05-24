<template>
  <div class="page">
    <div class="hero__image">
      <div class="hero__text">
        <p class="company__name">Connecting Farmers</p>
        <p class="page__title">Portfolio</p>
        <p class="title-sub-text mx-4">
          At SUBA Capital we offer a wide range of amazing savings and
          investment plans for agricultural produces with returns from 10% to
          20% depending on the plan you choose.
        </p>
      </div>
    </div>
    <section id="faq-question" style="background: #f9fafa">
      <v-container>
      <our-current-stats />
      <our-strategy />
      <portfolio-slide class="my-8 mt-md-8 mb-md-4" />
      </v-container>
    </section>
  </div>
</template>

<script>
import OurCurrentStats from "../components/includes/ourCurrentStats.vue";
import OurStrategy from '../components/includes/ourStrategy.vue';
import PortfolioSlide from '../components/includes/portfolio-slide.vue';
export default {
    name: "portfolio",
    data() {
        return {
        //
        };
    },
    components: { OurCurrentStats, OurStrategy, PortfolioSlide }
};
</script>

<style scoped>
.page {
  min-height: 100vh;
  width: 100%;
  margin-bottom: 120px;
}
.hero__image {
  position: relative;
  height: 50vh;
  width: 100vw;
  overflow: hidden;
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("/images/pages/hero/portfolio.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.hero__text {
  top: 30%;
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
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #17152a;
}
.title-sub-text {
  max-width: 40rem;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  text-align: center;


  /* WHITE */

  color: #ffffff;
}

.v-text-field--rounded {
  border-radius: 8px !important;
}
.v-label {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
}
</style>
