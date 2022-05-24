<template>
  <v-row class="d-flex justify-center align-center">
    <v-col cols="10">
      <v-item-group>
        <v-row class="d-flex justify-md-space-around align-center">
          <v-col v-for="item in articles" :key="item.src" cols="12" md="4">
            <v-item v-slot="{ active }">
              <v-card
                nuxt
                class="pa-0"
                :rounded="round[$vuetify.breakpoint.name]"
                :hover="active ? 'elevation-4' : false"
                @click="openBlog"
              >
                <v-img
                  :src="item.src"
                  class="white--text align-end"
                  gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                  height="230px"
                >
                </v-img>
                <p
                  class="article__created px-8 py-2"
                  v-text="item.created_at"
                ></p>
                <p
                  class="article__title px-8 pt-2 pb-6"
                  v-text="item.title"
                ></p>
              </v-card>
            </v-item>
          </v-col>
        </v-row>
      </v-item-group>
    </v-col>
  </v-row>
</template>

<script>
export default {
  props: {},
  name: "",
  data() {
    return {
      model: null,
      round: {
        xs: "sm",
        md: "xl",
      },
      cards: [
        { src: "/images/gallery/pix2.jpg" },
        { src: "/images/gallery/pix3.jpg" },
        { src: "/images/gallery/pix4.jpg" },
        { src: "/images/gallery/pix5.jpg" },
        { src: "/images/gallery/pix6.jpg" },
        { src: "/images/gallery/pix7.jpg" },
        { src: "/images/gallery/pix8.jpg" },
        { src: "/images/gallery/pix9.jpg" },
      ],
      articles: [
        {
          src: "/images/gallery/pix2.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "11 Jan, 2022",
        },
        {
          src: "/images/gallery/pix3.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "15 Jan, 2022",
        },
        {
          src: "/images/gallery/pix4.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "15 Jan, 2022",
        },
        {
          src: "/images/gallery/pix5.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "15 Jan, 2022",
        },
        {
          src: "/images/gallery/pix6.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "15 Jan, 2022",
        },
        {
          src: "/images/gallery/pix7.jpg",
          title: "Agriculture Matters to the Future of next",
          created_at: "31 Jan, 2022",
        },
      ],
    };
  },

  methods: {
    openBlog() {
      var string = this.articles[0].title;
      string = string.replaceAll(" ", "_");
      console.log(this.$route);
      this.$router.push(`/blog/${string}`);
    },
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
.article__created {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 14px;

  text-transform: capitalize;
  color: #908daa;
}
.article__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: bold;
  font-weight: 750;
  font-size: 24px;
}
</style>
