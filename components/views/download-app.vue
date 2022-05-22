<template>
  <div class="download-app">
    <v-container>
      <v-row class="d-flex justify-sm-space-around align-center">
        <v-col cols="12" md="7" order="2" order-md="1">
          <div class="download-message px-10 px-md-auto">
            <p class="header text-center text-md-start">Dreams Come True With SUBA Capital</p>
            <p>
              <v-icon :size="size[$vuetify.breakpoint.name]" color="#8E48A0">mdi-checkbox-marked</v-icon
              ><span class="body-text px-2"
                >Create an account via our app available on Google Playstore or
                Appstore.</span
              >
            </p>
            <p>
              <v-icon :size="size[$vuetify.breakpoint.name]" color="#8E48A0">mdi-checkbox-marked</v-icon
              ><span class="body-text px-2"
                >Select an investment option and fund the investment.</span
              >
            </p>
            <p>
              <v-icon :size="size[$vuetify.breakpoint.name]" color="#8E48A0">mdi-checkbox-marked</v-icon
              ><span class="body-text px-2"
                >Lastly, track and manage your investments.</span
              >
            </p>
            <div class="play-store">
              <a
                href="https://play.google.com/store/apps/details?id=com.dstvmobile.android&pcampaignid=pcampaignidMKT-Other-global-all-co-prtnr-py-PartBadge-Mar2515-1"
                ><img
                  alt="Get it on Google Play"
                  src="https://play.google.com/intl/en_us/badges/static/images/badges/en_badge_web_generic.png"
              /></a>

              <a style="align-self: center"
                href="https://apps.apple.com/us/app/wikipedia/id324715238?itsct=apps_box_badge&amp;itscg=30200"
                ><img
                  src="https://tools.applemediaservices.com/api/badges/download-on-the-app-store/black/en-us?size=250x83&amp;releaseDate=1250467200&h=d4c88f091ec0f6af1feeb784ed7adc94"
                  alt="Download on the App Store"
                  style="
                    border-radius: 13px;
                    width: 190px;
                  "
              /></a>
            </div>
          </div>
        </v-col>
        <v-col cols="12" md="5" order="1" order-md="2" class="px-auto px-md-0">
          <img class="app-image" src="/images/downloadappimage.png" alt="phone-image">
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  name: "download-app",
  data(){
    return {
      size: {
        sm: "small",
        md: "large"
      }
    }
  }
};
</script>

<style scoped>
.download-app {
  padding: 0;
  margin: 0;
}

.download-message .header {
  font-size: 2.5rem;
  font-weight: bolder;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  /* padding-top: 152px; */
  padding-bottom: 56px;

  text-align: start;
  color: #1a1544;
}
.body-text {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 22px;
  line-height: 20px;
  color: #4d4877;
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
.play-store {
  display: flex;
  align-content: center;
  margin: 0;
}
.play-store img {
  width: 15rem;
  height: auto;
  padding-top: 0;
  align-self: center;
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
 .download-message .header {
  font-size: 2.0rem;
  font-weight: bolder;
  padding-bottom: 44px;
}
.body-text {
  font-size: 18px;
  line-height: 16px;
}
}
</style>
