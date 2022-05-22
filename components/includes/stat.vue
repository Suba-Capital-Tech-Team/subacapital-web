<template>
  <v-row>
    <v-col cols="12" md="8" offset-md="2">
      <v-row>
        <v-col cols="12" md="3" class="pa-0">
          <img
            src="/images/gallery/stat.jpg"
            alt=""
            class="rounded-bl-lg rounded-tl-lg"
          />
        </v-col>
        <v-col cols="12" md="9" class="pa-0">
          <div
            class="pa-0 d-block d-md-flex justify-center justify-md-space-around align-center py-md-10 pr-md-8 rounded-br-lg rounded-tr-lg"
            style="background: #e1ead7; width: 100%; height: 100%"
          >
            <div
              class="stat__cards d-flex flex-column justify-center align-center"
            >
              <span class="analytics__box--title">
                <ICountUp :delay="delay" :endVal="500" :options="options" />
              </span>
              <span class="analytics__box--text"> farmlands</span>
            </div>
            <v-divider class="mx-4" vertical></v-divider>
            <div
              class="stat__cards d-flex flex-column justify-center align-center"
            >
              <span class="analytics__box--title">
                <ICountUp :delay="delay" :endVal="100" :options="options" />+
              </span>
              <span class="analytics__box--text"> farmers</span>
            </div>
            <v-divider class="mx-4" vertical></v-divider>
            <div
              class="stat__cards d-flex flex-column justify-center align-center"
            >
              <span class="analytics__box--title">
                <ICountUp :delay="delay" :endVal="200" :options="options" />
              </span>
              <span class="analytics__box--text"> farmlands</span>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
import ICountUp from "vue-countup-v2";
export default {
  components: {
    ICountUp,
  },
  data() {
    return {
      delay: 1000,
      endVal: 1050,
      options: {
        useEasing: true,
        useGrouping: true,
        separator: ",",
        decimal: ".",
        prefix: "",
        suffix: "",
      },
    };
  },
};
</script>

<style scoped>
.analytics__box--title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 36px;
  line-height: 43px;
  text-transform: capitalize;
}
.analytics__box--text {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  text-transform: capitalize;
}
</style>
