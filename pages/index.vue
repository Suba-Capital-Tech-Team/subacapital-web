<template>
  <div class="page">
    <div class="hero">
      <div class="hero__cover">
        <div class="py-md-2 text-h3 text-md-h2 text-white text-center">
          <p class="hero-heading pt-4">
            A new way of <br />
            <span class="">investing in the future.</span>
          </p>
        </div>
        <div class="my-6 my-md-6 text-h6 text-md-h5 text-white text-center">
          <p>
            We’re creating a new approach to investing; by giving investors the
            <br />
            oppurtunity to invest in agricultural farms thereby increasing food
            production
          </p>
        </div>

        <v-btn
          color="primary"
          dark
          class="text-button py-8 rounded-lg font-weight-medium"
          elevation="1"
          x-large
          >Explore our Investment plans</v-btn
        >
      </div>
    </div>

    <video-section
      :sectionBody="description"
      :sectionTitle="title"
      :button="button"
    />
    <section class="section-wwo ">
      <what-we-offer :button="button" class="" />
      <download-app class="py-4 py-md-12 mt-md-10" />
    </section>
    <section class="section-testimonials">
      <client-only placeholder="Loading...">
      <testiminial />
      </client-only>
    </section>
    <section class="section-gallery pb-2 pb-md-16">
      <gallery-sect />
    </section>
    <section class="section-news-article pb-2 pb-md-16">
      <our-news-page />
    </section>
    <section class="section-partners pb-2 pb-md-16">
      <partners />
    </section>
  </div>
</template>

<script>
import Partners from '../components/includes/partners.vue';
import videoSection from "../components/video-section.vue";
import DownloadApp from "../components/views/download-app.vue";
import GallerySect from '../components/views/gallery-sect.vue';
import OurNewsPage from '../components/views/our-news-page.vue';
import Testiminial from "../components/views/testiminial.vue";
import WhatWeOffer from "../components/views/what-we-offer.vue";
export default {
  components: { videoSection, WhatWeOffer, DownloadApp, Testiminial, GallerySect, OurNewsPage, Partners },
  name: "IndexPage",
  data() {
    return {
      image: "https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg",
      description:
        "At Suba Capital we  use the invested funds to secure farm lands, engage farm workers, plant crops, insure farm workers and farm produce, complete a full farming cycle and harvest sales logistics.",
      title: "Now you can save and invest in agriculture",
      button: "Learn More",
    };
  },
};
</script>

<style scoped>
.no-ssr-placeholder {
  color: #41b883;
}
.page {
  min-height: 100vh;
  width: 100%;
}
.hero {
  position: relative;
  height: 70vh;
  width: 100vw;
  overflow: hidden;
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("/images/pages/index/homePage.jpg");
  background-size: cover;
  background-position: center;
}
.hero__cover {
  position: absolute;
  padding: 40px 25px;
  height: auto;
  width: 100%;
  background-color: #0d0d0d 65;
  text-align: center;
}
.hero__cover div {
  max-width: 100%;
}

.hero-heading {
  font-family: "Roboto" sans-serif;
  font-style: bold;
  font-weight: 950;
  line-height: 100%;
}
</style>
