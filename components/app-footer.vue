<template>
  <v-footer color="#373166" absolute padless app>
    <v-container>
      <v-row
        class="d-flex justify-start justify-md-space-around align-center mx-4 mx-md-0 pa-0"
        no-gutters
      >
        <v-col cols="12" sm="6" md="3" class="px-0">
          <div class="footer__logo py-3 py-md-8">
            <img src="/images/footer-logo.png" alt="footer_logo" />
          </div>
          <div class="footer__address py-3 py-md-4">
            Address: 2 Adewale Taiwo Olajide Close, off Niyi Okunubi.
          </div>
          <div class="footer__contact py-3 py-md-2">
            support@subacapital.com <br />
            NG: +234 704 2629 950
          </div>
        </v-col>
        <v-col cols="12" sm="6" md="9" class="px-0">
          <v-row class="d-flex mt-8 mt-md-0 mx-auto pa-0">
            <v-col cols="12" sm="6" md="4" class="px-0">
              <span class="footer__title">Company</span>
              <ul>
                <li>
                  <router-link to="/" class="footer__links">Home</router-link>
                </li>
                <li>
                  <router-link to="/about-us" class="footer__links"
                    >About Us</router-link
                  >
                </li>
                <li>
                  <router-link to="/contact" class="footer__links"
                    >Contact Us</router-link
                  >
                </li>

                <li>
                  <router-link to="/portfolio" class="footer__links"
                    >Portfolio</router-link
                  >
                </li>
              </ul>
            </v-col>
            <v-col cols="12" sm="6" md="4" class="px-0">
              <span class="footer__title mt-8 mt-md-0">Quick links</span>
              <ul>
                <li>
                  <router-link to="/faq" class="footer__links">FAQ</router-link>
                </li>
                <li>
                  <router-link to="/blog" class="footer__links">
                    Blog
                  </router-link>
                </li>
              </ul>
            </v-col>
            <v-col cols="12" sm="6" md="4" class="px-0">
              <span class="footer__title mt-8 pt-md-0"> Our Newsletter </span>
              <span
                class="footer__links d-block py-3"
                style="line-height: 2rem"
              >
                Subscribe to our newsletter and we will inform you about latest
                updates and offers
              </span>
              <v-text-field
                dark
                name="Email Address"
                type="email"
                light
                outlined
                label="Email Address"
                append-icon="mdi-arrow-right"
                hide-details="auto"
                class="mt-5 pa-0 ma-0"
                elevation="0"
              ></v-text-field>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <div
        class="flex flex-col md:flex-row gap-5 justify-between py-10 items-center"
      >
        <span class="copyright">
          &copy; {{ new Date().getFullYear() }} SUBA Capital Limited. All rights
          reserved.
        </span>

        <div>
          <v-btn dark icon><v-icon>mdi-facebook</v-icon></v-btn>
          <v-btn dark icon><v-icon>mdi-instagram</v-icon></v-btn>
          <v-btn dark icon><v-icon>mdi-twitter</v-icon></v-btn>
        </div>
      </div>
    </v-container>
  </v-footer>
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
.footer__address {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #ffffff;
  width: 250px;
}
.footer__contact {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
  color: #ffffff;
}
.footer__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 28px;
  line-height: 25px;
  color: #ffffff;
}
.footer__links {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 300;
  font-size: 22px;
  line-height: 19px;
  text-transform: capitalize;

  color: #ffffff;
}
ul {
  padding-left: 0px;
}
ul li {
  padding-right: 0px;
  margin-top: 20px;
}
.copyright {
  font-size: 15px;
  color: #fafafa;
}

.v-footer {
  margin-top: 20vh;
}
@media only screen and (min-width: 768px) {
  .v-footer {
    margin-top: 5vh;
  }
  .footer__address .footer__contact {
    font-size: 16px;
  }
  .footer__title {
    font-size: 22px;
  }

  .footer__links {
    font-size: 16px;
  }
}
</style>
