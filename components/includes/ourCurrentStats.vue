<template>
  <div class="">
    <div class="text-center section__title">Our Current portfolio</div>
    <v-row>
      <v-col cols="12" sm="6" md="3">
        <v-card
          rounded="lg"
          elevation="5"
          class="d-flex flex-column justify-center align-center"
        >
          <span class="figure pt-5 pb-3">&#8358;100M</span>
          <span class="note">Asset Under Management</span>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6" md="3">
        <v-card
          rounded="lg"
          elevation="5"
          class="d-flex flex-column justify-center align-center"
        >
          <span class="figure pt-5 pb-3">40</span>
          <span class="note">Hectares of Farmland</span>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6" md="3">
        <v-card
          rounded="lg"
          elevation="5"
          class="d-flex flex-column justify-center align-center"
        >
          <span class="figure pt-5 pb-3">1</span>
          <span class="note">Commodity(Maize)</span>
        </v-card>
      </v-col>
      <v-col cols="12" sm="6" md="3">
        <v-card
          rounded="lg"
          elevation="5"
          class="d-flex flex-column justify-center align-center"
        >
          <span class="figure pt-5 pb-3">&#8358;6.6M</span>
          <span class="note">Gross Volume Traded</span>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      //
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");
.figure {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 48px;
  line-height: 58px;
  text-align: center;
  color: rgba(33, 26, 85, 1);
}
.note {
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 24px;
  line-height: 58px;
  text-align: center;
  color: rgba(33, 26, 85, 1);
}
.section__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 36px;
  line-height: 43px;
  color: rgba(33, 26, 85, 1);
  padding-top: 71px;
  padding-bottom: 68px;
}
.v-application .elevation-5 {
  box-shadow: 0px 3px 5px -1px rgb(0 0 0 / 7%),
    0px 5px 8px 0px rgb(0 0 0 / 3%), 0px 1px 14px 0px rgb(0 0 0 / 2%) !important;
}
</style>
