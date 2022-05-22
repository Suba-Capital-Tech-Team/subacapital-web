<template>
  <div class="testimonial d-flex justify-center align-start align-md-center">
    <v-container fluid>
      <v-row class="d-flex justify-center align-center py-4 py-md-0">
        <v-col cols="12" md="4">
          <div
            class="test__left d-flex justify-center flex-column align-center align-md-start text-center text-md-left"
          >
            <h6 class="pt-2 pt-md-0 px-md-12">OUR TESTIMONIALS</h6>
            <p class="px-auto px-md-12" v-if="$vuetify.breakpoint.mdAndUp">
              What they’re talking about SUBA Capital
            </p>
            <div
              v-if="$vuetify.breakpoint.mdAndUp"
              class="control d-flex justify-start align-center px-auto px-md-12"
              style="width: 50%"
            >
              <v-icon
                large
                tag="button"
                @click.prevent="$refs.prev.click()"
                class="prev"
                >mdi-arrow-left-thin-circle-outline</v-icon
              >
              <v-icon
                large
                tag="button"
                @click.prevent="$refs.next.click()"
                class="next"
                >mdi-arrow-right-thin-circle-outline</v-icon
              >
            </div>
          </div>
        </v-col>

        <v-col
          cols="12"
          sm="4"
          md="8"
          class="d-flex justify-center align-center"
        >
          <v-slide-group
            v-model="model"
            center-active
            v-if="$vuetify.breakpoint.smAndDown"
          >
            <v-slide-item v-for="card in cards" :key="card.clientName">
              <slide-cards
                class="mb-8 mb-md-0"
                :avatar="card.avatar"
                :message="card.message"
                :title="card.title"
                :client="card.clientName"
              />
            </v-slide-item>
          </v-slide-group>
          <div
            class="overflow-hidden d-flex justify-center align-center"
            v-if="$vuetify.breakpoint.mdAndUp"
          >
            <div>
              <no-ssr>
                <!-- important to add no-ssr-->

                <carousel
                  :responsive="resp"
                  :dots="false"
                  :autoplay="true"
                  :loop="true"
                  :items="4"
                  :center="true"
                  :nav="false"
                >
                  <template slot="prev">
                    <span hidden ref="prev" class="prev">prev</span>
                  </template>

                  <div
                    v-for="(card, i) in cards"
                    :key="i"
                    class="mx-0 mb-16 mb-md-0"
                  >
                    <slide-cards
                      :avatar="card.avatar"
                      :message="card.message"
                      :title="card.title"
                      :client="card.clientName"
                    />
                  </div>
                  <template slot="next"
                    ><span hidden ref="next" class="next">next</span></template
                  >
                </carousel>
              </no-ssr>
            </div>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import slideCards from "../includes/slide-cards.vue";
export default {
  components: { slideCards },
  props: {},
  name: "testimonials",
  data() {
    return {
      model: null,
      resp: { 0: { items: 1, nav: false }, 600: { items: 3.5, nav: false } },
      cards: [
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc?img=25",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "Paul Morgan",
        },
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc/300",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "Kazeem Daniel",
        },
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc/300?img=7",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "Ken Shiroku",
        },
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc/300?img=10",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "Nedu Osas",
        },
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc/300?img=64",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "kay Johnson",
        },
        {
          title: "Farmer",
          avatar: "https://i.pravatar.cc/300?img=3",
          message:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quaerat dicta in consectetur magnam dolore non velit ex voluptatibus tenetur molestiae libero, officiis nisi. Quia iste tempore exercitationem accusamus nulla dolor",
          clientName: "Josh Victor",
        },
      ],
      direction: "forward",
      frame: 2,
      count: 0,
    };
  },
};
</script>

<style scoped>
.testimonial {
  width: 100%;
  height: 70vh;
  padding: 0;
  margin: 0;
  background: url("/images/pages/index/testimonial-bg.jpg"),
    linear-gradient(rgba(242, 241, 235, 0.9), rgba(242, 241, 235, 0.9));
  background-blend-mode: overlay;
  background-size: cover;
  background-position: center;
}

.test__left {
  width: 100%;
  height: auto;
}
.test__left h6 {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: bold;
  font-weight: 700;
  font-size: 18px;
  line-height: 22px;
  /* identical to box height */
  color: rgba(33, 26, 85, 1);

  text-transform: uppercase;
}
/*Small smartphones [325px -> 425px]*/
@media only screen and (max-width: 425px) {
  .test__left h6 {
    font-weight: 700;
    font-size: 18px;
    line-height: 14px;
  }

  .test__left p {
    font-weight: 500;
    font-size: 12px;
    line-height: 31px;
  }
}
/*Big smartphones [426px -> 600px]*/
@media only screen and (max-width: 600px) {
  .test__left h6 {
    font-weight: 700;
    font-size: 24px;
    text-transform: uppercase;
  }
  .test__left p {
    font-weight: 500;
    font-size: 12px;
    line-height: 26px;
  }
}
.test__left p {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 48px;
  line-height: 63px;
  color: rgba(33, 26, 85, 1);
}
.v-application .elevation-6 {
  box-shadow: 0px 3px 3px -2px rgb(0 0 0 / 2%), 0px 3px 4px 0px rgb(0 0 0 / 6%),
    0px 1px 10px 0px rgb(0 0 0 / 4%) !important;
}
.btn {
  width: 35px;
  height: 35px;
}
</style>
