<template>
  <v-container fluid>
    <h5 class="gallery-title text-center pt-4 pt-md-16 mt-md-14 pb-2 pb-md-8">
      Our Gallery
    </h5>
    <v-row class="d-flex justify-center align-center">
      <v-col cols="12">
        <v-slide-group
          v-model="model"
          class="px-1 pa-md-4"
          active-class="success"
          mobile-breakpoint="500"
        >
          <v-slide-item v-for="n in cards" :key="n.src">
            <v-card class="mx-3 ma-md-4 rounded-lg" height="253" width="285">
              <v-img :src="n.src" height="100%" width="100%"> </v-img>
            </v-card>
          </v-slide-item>
        </v-slide-group>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {},
  name: "gallery-sect",
  data() {
    return {
      model: null,
      cards: [
        { src: "/images/gallery/pix2.jpg" },
        { src: "/images/gallery/pix3.jpg" },
        { src: "/images/gallery/pix4.jpg" },
        { src: "/images/gallery/pix5.jpg" },
        { src: "/images/gallery/pix6.jpg" },
        { src: "/images/gallery/pix7.jpg" },
      ],
    };
  },
};
</script>

<style scoped>
.gallery-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: bold;
  font-weight: 750;
  font-size: 36px;
  line-height: 53px;
  text-transform: capitalize;
}
.v-application .elevation-6 {
  box-shadow: 0px 3px 3px -2px rgb(0 0 0 / 2%), 0px 3px 4px 0px rgb(0 0 0 / 6%),
    0px 1px 10px 0px rgb(0 0 0 / 4%) !important;
}
.btn {
  width: 35px;
  height: 35px;
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .gallery-title {
    font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
    font-style: bold;
    font-weight: 750;
    font-size: 28px;
    text-transform: capitalize;
  }
}
</style>
