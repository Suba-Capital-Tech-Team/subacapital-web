<template>
  <div class="what-we-offer">
    <h3>what we offer</h3>
    <v-container>
      <v-row
        class=" d-flex justify-center justify-md-space-around"
      >
        <v-col class="d-flex justify-center px-auto" cols="12" sm="6" md="4"
          ><v-card elevation="6" rounded="lg" flat width="410">
            <v-avatar size="60" tile class="mt-15 mx-10">
              <img src="/images/fluent_savings-24-filled.png" alt="John" />
            </v-avatar>
            <v-card-title class="card-title pt-5 px-10"> savings </v-card-title>
            <v-card-text class="card-text px-10">
              We use the invested funds to secure farm toland, engage farm
              workers, plant crops,
            </v-card-text>
            <v-card-actions class="px-10 py-10">
              <v-btn color="primary" outlined class="text-capitalize">
                <span class="primary--text font-weight-bold">
                  {{ button }}
                </span>
              </v-btn>
            </v-card-actions>
          </v-card></v-col
        >
        <v-col class="d-flex justify-center px-auto" cols="12" sm="6" md="4"
          ><v-card elevation="6" rounded="lg" flat width="410">
            <v-avatar size="60" tile class="mt-15 mx-10">
              <img src="/images/fluent_savings-24-filled.png" alt="John" />
            </v-avatar>
            <v-card-title class="card-title pt-5 px-10">
              Investments
            </v-card-title>
            <v-card-text class="card-text px-10">
              We use the invested funds to secure farm toland, engage farm
              workers, plant crops,
            </v-card-text>
            <v-card-actions class="px-10 py-10">
              <v-btn color="primary" outlined class="text-capitalize">
                <span class="primary--text font-weight-bold">
                  {{ button }}
                </span>
              </v-btn>
            </v-card-actions>
          </v-card></v-col
        >
        <v-col class="d-flex justify-center px-auto" cols="12" sm="6" md="4"
          ><v-card elevation="6" rounded="lg" flat width="410">
            <v-avatar size="60" tile class="mt-15 mx-10">
              <img src="/images/fluent_savings-24-filled.png" alt="John" />
            </v-avatar>
            <v-card-title
              class="card-title pt-5 px-10 text-center text-md-start"
            >
              peer to peer loans
            </v-card-title>
            <v-card-text class="card-text px-10">
              We use the invested funds to secure farm toland, engage farm
              workers, plant crops,
            </v-card-text>
            <v-card-actions class="px-10 py-10">
              <v-btn color="primary" outlined class="text-capitalize">
                <span class="primary--text font-weight-bold">
                  {{ button }}
                </span>
              </v-btn>
            </v-card-actions>
          </v-card></v-col
        >
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  props: {
    button: String,
  },
  name: "wwo-section",
};
</script>

<style scoped>
.what-we-offer h3 {
  font-size: 2.5rem;
  font-weight: bolder;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  padding-top: 152px;
  padding-bottom: 64px;

  text-align: center;
  color: #1a1544;
}
.avatar {
  padding-left: 120px;
  border-radius: 8px;
}
.card-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: bold;
  font-size: 24px;
  line-height: 29px;
  text-transform: capitalize;
  color: #1a1544;
}
.card-text {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #908daa;
}
.v-application .elevation-6 {
  box-shadow: 0px 3px 3px -2px rgb(0 0 0 / 2%), 0px 3px 4px 0px rgb(0 0 0 / 6%),
    0px 1px 10px 0px rgb(0 0 0 / 4%) !important;
}
@media only screen and (max-width: 768px) {
.what-we-offer h3 {
  font-size: 2.0rem;
  padding-top: 64px;
  padding-bottom: 32px;
  text-align: center;
  color: #1a1544;
}

}
</style>
