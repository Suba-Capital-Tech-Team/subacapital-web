<template>
  <v-app-bar
    id="app"
    :height="75"
    width="100%"
    color="#fff"
    app
    dense
    
    :elevate-on-scroll="elevateOnScroll"
  >
    <div class="app-header md:px-10 flex items-center">
      <router-link to="/">
        <img class="app-header__logo" src="/images/logo.svg" alt=""
      /></router-link>
      <v-spacer></v-spacer>
      <div class="hidden md:flex">
        <v-hover v-slot="{ hover }">
          <nuxt-link to="/">
            <v-btn
              class="link-text font-sans"
              rounded
              :ripple="false"
              :color="hover || $route.name == 'home' ? 'primary' : '#000000'"
              text
              >Home</v-btn
            >
          </nuxt-link>
        </v-hover>
        <v-hover v-slot="{ hover }">
          <nuxt-link to="/about-us">
            <v-btn
              class="link-text"
              rounded
              :ripple="false"
              :color="
                hover || $route.name == 'about-us' ? 'primary' : '#000000'
              "
              text
              >About Us</v-btn
            >
          </nuxt-link>
        </v-hover>

        <v-hover v-slot="{ hover }">
          <nuxt-link to="/portfolio">
            <v-btn
              class="link-text"
              rounded
              :ripple="false"
              :color="
                hover || $route.name == 'portfolio' ? 'primary' : '#101010'
              "
              text
              >Portfolio</v-btn
            >
          </nuxt-link>
        </v-hover>

        <v-hover v-slot="{ hover }">
          <nuxt-link to="/blog">
            <v-btn
              class="link-text"
              rounded
              :ripple="false"
              :color="hover || $route.name == 'blog' ? 'primary' : '#101010'"
              text
              >Blog</v-btn
            >
          </nuxt-link>
        </v-hover>
        <v-hover v-slot="{ hover }">
          <nuxt-link to="/faq">
            <v-btn
              class="link-text"
              rounded
              :ripple="false"
              :color="hover || $route.name == 'faq' ? 'primary' : '#101010'"
              text
              >FAQ</v-btn
            >
          </nuxt-link>
        </v-hover>
      </div>

      <div class="mx-8 hidden md:flex">
        <v-btn
          class="rounded-lg text-capitalize"
          dark
          large
          to="/contact"
          elevation="0"
          color="#541592"
          >Contact Us</v-btn
        >
      </div>

      <span class="inline-flex md:hidden" ref="menu">
        <v-btn @click="showPopup = !showPopup" icon>
          <v-icon large>mdi-menu</v-icon>
        </v-btn>
      </span>
    </div>
    <div
      class="mobile-popup shadow-md"
      ref="popup"
      :class="{ 'mobile-popup--show': showPopup }"
    >
      <div class="link-text mx-5 mobile-popup__links">
        <router-link to="/"> Home </router-link>
        <router-link to="/about-us"> About Us </router-link>
        <router-link to="/contact"> Contact Us </router-link>
        <router-link to="/portfolio"> Portfolio </router-link>
        <router-link to="/blog"> Blog </router-link>
        <router-link to="/faq"> FAQ</router-link>
      </div>
    </div>
  </v-app-bar>
</template>

<script>
export default {
  data() {
    return {
      showPopup: false,
      elevateOnScroll: true,
    };
  },
  mounted() {
    setTimeout(() => {
      this.$nextTick(() => {
        document.addEventListener("click", (event) => {
          try {
            if (
              !this.$refs.popup.contains(event.target) &&
              !this.$refs.menu.contains(event.target)
            ) {
              this.showPopup = false;
            }
          } catch (e) {
            this.showPopup = false;
          }
        });
      });
    }, 1000);
  },
  watch: {
    $route() {
      this.showPopup = false;
    },
  },
};
</script>

<style scoped>
.link-text {
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 16px;
  line-height: 19px;

  color: #000000;
}
.app-header__logo {
  width: auto;
  height: 150px;
  margin-right: 20px;
}
.mobile-popup {
  width: 100%;
  background-color: #fff;
  position: fixed;
  top: 75px;
  left: 0;
  display: none;
  padding: 10px;
}
.mobile-popup--show {
  display: block;
}
.mobile-popup__links a {
  display: block;
  padding: 10px;
}
</style>
