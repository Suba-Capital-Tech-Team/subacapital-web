<template>
  <div class="my-8 my-md-16">
    <div>
      <p class="sub-title">What we are all about</p>
      <p class="sect__title">Our Core Values</p>
    </div>
    <div>
      <v-row>
        <v-col cols="12" md="8" offset-md="2">
          <v-row>
            <v-col cols="12" sm="6" md="4">
              <v-card
                elevation="6"
                class="d-flex flex-column justify-center text-center align-center mx-4 mx-md-8 rounded-lg"
              >
                <v-avatar color="grey" tile size="80" class="mt-8 rounded-lg">
                  <v-icon x-large dark> mdi-briefcase-check-outline </v-icon>
                </v-avatar>
                <v-card-title class="card__title"> Investments </v-card-title>
                <v-card-text class="card__text pb-10">
                  We use the invested funds to secure farm toland, engage farm
                  workers, plant crops,
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="6" md="4">
              <v-card
                elevation="6"
                class="d-flex flex-column justify-center text-center align-center mx-4 mx-md-8 rounded-lg"
              >
                <v-avatar color="grey" tile size="80" class="mt-8 rounded-lg">
                  <v-icon x-large dark> mdi-briefcase-check-outline </v-icon>
                </v-avatar>
                <v-card-title class="card__title"> Investments </v-card-title>
                <v-card-text class="card__text pb-10">
                  We use the invested funds to secure farm toland, engage farm
                  workers, plant crops,
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="6" md="4">
              <v-card
                elevation="6"
                class="d-flex flex-column justify-center text-center align-center mx-4 mx-md-8 rounded-lg"
              >
                <v-avatar color="grey" tile size="80" class="mt-8 rounded-lg">
                  <v-icon x-large dark> mdi-briefcase-check-outline </v-icon>
                </v-avatar>
                <v-card-title class="card__title"> Investments </v-card-title>
                <v-card-text class="card__text pb-10">
                  We use the invested funds to secure farm toland, engage farm
                  workers, plant crops,
                </v-card-text>
              </v-card>
            </v-col>
            
          </v-row>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.sub-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #908daa;
  text-align: center;
}
.sect__title {
  font-size: 2.5rem;
  font-weight: bolder;
  font-style: normal;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  padding-top: 8px;
  padding-bottom: 64px;
  text-align: center;
  color: #1a1544;
}
.card__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 24px;
  line-height: 29px;
  text-transform: capitalize;
  color: #1a1544;
}
.card__text {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 22px;
  text-align: center;
  color: #908daa;
}
.v-application .elevation-6 {
  box-shadow: 0px 3px 3px -2px rgb(0 0 0 / 2%), 0px 3px 4px 0px rgb(0 0 0 / 6%),
    0px 1px 10px 0px rgb(0 0 0 / 4%) !important;
}
</style>
