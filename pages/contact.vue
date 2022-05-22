<template>
  <div class="page">
    <div class="hero__image">
      <div class="hero__text">
        <p class="company__name">SUBA CAPITAL</p>
        <p class="page__title">Contact us</p>
      </div>
    </div>

    <v-row class="px-auto d-flex justify-center align-center">
      <v-col cols="12" md="8">
        <v-row>
          <v-col cols="12" md="4">
            <div class="mx-8 mx-md-0" style="max-width: 350px; margin-top: 92px">
              <p class="sub-title">Connecting Farmers</p>
              <p class="sect__title">Get in Touch with Us</p>
              <p class="sect__body">
                We are committed to providing our customers with exceptional
                service.
              </p>
            </div>
          </v-col>
          <v-col cols="12" md="8">
            <div class="px-8 px-md-0" style="margin-top: 92px">
              <form action="">
                <v-row class="d-flex justify-center align-center">
                  <v-col cols="12" md="6" class="mx-0">
                    <v-text-field
                      hide-details="auto"
                      background-color="#F5F7FA"
                      v-model="contact.firstName"
                     outlined
                      label="First Name"
                      filled
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" md="6" class="mx-0">
                    <v-text-field
                      hide-details="auto"
                      background-color="#F5F7FA"
                      v-model="contact.lastName"
                     outlined
                      label="Last Name"
                      filled
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" class="mx-0">
                    <v-text-field
                      hide-details="auto"
                      background-color="#F5F7FA"
                      v-model="contact.phone"
                     outlined
                      label="Phone Number"
                      filled
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" class="mx-0">
                    <v-text-field
                      hide-details="auto"
                      background-color="#F5F7FA"
                      v-model="contact.subject"
                     outlined
                      label="Subject"
                      filled
                    ></v-text-field>
                  </v-col>
                  <v-col cols="12" class="mx-0">
                    <v-textarea
                      hide-details="auto"
                      background-color="#F5F7FA"
                      v-model="contact.message"
                     outlined
                      label="Write Your Message"
                      filled
                    ></v-textarea>
                  </v-col>
                  <v-col cols="12" class="mx-0">
                    <v-btn
                      color="primary"
                      dark
                      x-large
                      class="px-11 text-capitalize"
                    >
                      Send a message
                    </v-btn>
                  </v-col>
                </v-row>
              </form>
            </div>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  name: "contact",
  data() {
    return {
      contact: {
        firstName: "",
        lastName: "",
        phone: "",
        subject: "",
        message: "",
      },
    };
  },
};
</script>

<style scoped>
.page {
  min-height: 100vh;
  width: 100%;
  margin-bottom: 120px;
}
.hero__image {
  position: relative;
  height: 50vh;
  width: 100vw;
  overflow: hidden;
  background-image: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)),
    url("/images/pages/hero/contact.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
.hero__text {
  top: 50%;
  position: absolute;
  height: auto;
  width: 100%;
  background-color: #0d0d0d 65;
  text-align: center;
}
.company__name {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 33px;
  text-align: center;
  color: #ffffff;
}
.page__title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 48px;
  line-height: 33px;
  color: #ffffff;
}
.sub-title {
  font-family: "Roboto", sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  text-transform: uppercase;
  color: #17152a;
}
.sect__title {
  font-style: normal;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: 750;
  font-size: 36px;
  line-height: 43px;
  color: #1a1544;
  max-width: 35rem;
}
.sect__body {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
}
.v-text-field--rounded {
  border-radius: 8px !important;
}
.v-label {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 24px;
}
</style>
