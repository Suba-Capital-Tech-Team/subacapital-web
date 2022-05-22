<template>
  <v-row class="ma-0 pa-0 d-flex justify-center align-center">
    <v-col class="ma-0 pa-0" cols="12" md="10" offset-md="2">
      <v-carousel
        cycle
        height="500"
        hide-delimiter-background
        :show-arrows="false"
      >
        <v-carousel-item v-for="(slide, i) in slides" :key="i">
          <div class="d-block d-md-flex justify-center align-center">
            <div class="d-flex justify-center align-center">
              <img
                height="auto"
                :src="require(`~/static/images/portfolio-slide/${i + 1}.jpg`)"
                class="image-container"
              />
            </div>

            <div
              class="d-flex flex-column justify-center align-center text-center"
            >
              <h5 class="slide-title py-4 pt-md-2 pb-md-10">{{ slide }}</h5>
              <p class="text-h6 text-start px-md-10">
                We utilize 60% of our contibuted fundsin carrying out
                agribusiness(farming & commodity traade) activities. our annual
                production goal is to produce between 500 -100 tonnes of
                agricultural produce per farming cycle. We currently farm Maize
                and sell grain in commercial quantity. We started with 2 hectare
                farm in 2019, we are currently a 5 hectares per cycle expanding
                to 50 hectares of maize farm and looking to expand to 100
                hectares in the next 18 months with your support as an
                investment contributorz
              </p>

              <v-btn
                color="primary"
                large
                dark
                class="px-4 py-4 mt-md-6 mb-md-4 float-left"
              >
                Invest now
              </v-btn>
            </div>
          </div>
        </v-carousel-item>
      </v-carousel>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data() {
    return {
      //
      slides: [
        "Agri-business",
        "SME business Loan",
        "Social Media",
        "Farm to Prodution",
        "Yes, You can",
      ],
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");

.slide-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 42px;
  line-height: 58px;
  text-align: center;
  color: rgba(33, 26, 85, 1);
}

.image-container {
  border-radius: 25px 0 0 25px;
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
.image-container {
  border-radius: 25px;
}

.slide-title {
  font-weight: 500;
  font-size: 32px;
}
}
</style>
