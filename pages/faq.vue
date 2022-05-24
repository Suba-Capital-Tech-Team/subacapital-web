<template>
  <div class="page">
    <div class="hero__image">
      <div class="hero__text">
        <p class="company__name">SUBA CAPITAL</p>
        <p class="page__title">FAQ</p>
      </div>
    </div>

        <v-row class="py-8 my-8 py-md-10" style="background: #f1f0eb">
          <v-col
            cols="12"
            sm="6"
            md="4"
            v-for="item in contents"
            :key="item.title"
          >
            <faq-expansion :title="item.title" :answer="item.answer" />
          </v-col>
        </v-row>
  </div>
</template>

<script>
import faqExpansion from "../components/includes/faq-expansion.vue";
export default {
  components: { faqExpansion },
  name: "faq",
  data() {
    return {
      contents: [
        {
          title: "Agriculture Matters to the Future of next?",
          answer:
            "Suspendisse finibus urna mauris, vitae consequat quam vel. Vestibulum leo ligula, vitae commodo nisl. Lorem ipsum is simply free text available in the market adipisi cing elit.",
        },
        {
          title: "How do I subscribe?",
          answer:
            "Suspendisse finibus urna mauris, vitae consequat quam vel. Vestibulum leo ligula, vitae commodo nisl. Lorem ipsum is simply free text available in the market adipisi cing elit.",
        },
        {
          title: "Is there an insurance plan for investors?",
          answer:
            "Suspendisse finibus urna mauris, vitae consequat quam vel. Vestibulum leo ligula, vitae commodo nisl. Lorem ipsum is simply free text available in the market adipisi cing elit.",
        },
        {
          title: "What is the ROI for a year?",
          answer:
            "Suspendisse finibus urna mauris, vitae consequat quam vel. Vestibulum leo ligula, vitae commodo nisl. Lorem ipsum is simply free text available in the market adipisi cing elit.",
        },
      ],
    };
  },
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
    url("/images/pages/hero/contact.jpg");
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
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #17152a;
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
