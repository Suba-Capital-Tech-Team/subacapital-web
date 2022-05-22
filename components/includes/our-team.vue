<template>
  <div>
    <div class="pb-md-16 d-flex justify-center align-center">
      <p class="team-title">Meet Our Team</p>
    </div>
    <div class="d-flex justify-center align-center mx-auto mx-md-14 mb-4 mb-md-">
      <v-container>
        <v-row class="d-flex justify-center align-center ma-0 pa-0">
          <v-col
            class="pa-0 d-flex justify-center align-center"
            cols="12"
            sm="6"
            md="3"
          >
            <div class="polaroid justify-self-center">
              <div class="photo__container">
                <img
                  src="/images/our_team/silas.jpg"
                  alt="silas"
                  style="
                    width: 100%;
                    height: 100%;
                    border-top-left-radius: 14px;
                    border-top-right-radius: 14px;
                  "
                />
              </div>
              <div class="photo-details">
                <p class="team__name">Silas Ozoya</p>
                <span class="position"> CEO/Co-Founder </span>
              </div>
            </div>
          </v-col>
          <v-col
            class="pa-0 d-flex justify-center align-center"
            cols="12"
            sm="6"
            md="3"
          >
            <div class="polaroid justify-self-center">
              <div class="photo__container">
                <img
                  src="/images/our_team/judith.jpg"
                  alt="judith"
                  style="
                    width: 100%;
                    height: 100%;
                    border-top-left-radius: 14px;
                    border-top-right-radius: 14px;
                  "
                />
              </div>
              <div class="photo-details">
                <p class="team__name">Judith Adaku Ekwueme</p>
                <span class="position"> COO/Co-Founder </span>
              </div>
            </div>
          </v-col>
          <v-col
            class="pa-0 d-flex justify-center align-center"
            cols="12"
            sm="6"
            md="3"
          >
            <div class="polaroid justify-self-center">
              <div class="photo__container">
                <img
                  src="/images/our_team/richie.jpeg"
                  alt="richard"
                  style="
                    width: 100%;
                    height: 100%;
                    border-top-left-radius: 14px;
                    border-top-right-radius: 14px;
                  "
                />
              </div>
              <div class="photo-details">
                <p class="team__name">Richard Araromi</p>
                <span class="position"> CTO/Co-Founder </span>
              </div>
            </div>
          </v-col>
          <v-col
            class="pa-0 d-flex justify-center align-center"
            cols="12"
            sm="6"
            md="3"
          >
            <div class="polaroid justify-self-center">
              <div class="photo__container">
                <img
                  src="/images/our_team/samuel.jpg"
                  alt="richard"
                  style="
                    width: 100%;
                    height: 100%;
                    border-top-left-radius: 14px;
                    border-top-right-radius: 14px;
                  "
                />
              </div>
              <div class="photo-details">
                <p class="team__name">Sammuel Atusiuba</p>
                <span class="position"> Admin/Customer Support </span>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.team-title {
  font-style: normal;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: 750;
  font-size: 36px;
  line-height: 43px;
  color: #1a1544;
  max-width: 35rem;
  padding-top: 55px;
  padding-bottom: 55px;
}
div.polaroid {
  width: 320px;
  background-color: white;
  border-radius: 9px;
}

.team-details {
  text-align: center;
  padding: 10px 20px;
  display: flex;
  flex-direction: column;
  width: 100%;
}
.team__name {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 24px;
  line-height: 29px;
}
.position {
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 14px;
  text-transform: capitalize;
  color: #908daa;
}
.photo__container {
  height: 400px;
  width: 320px;
}
.photo-details {
  text-align: center;
  width: 320px;
  padding: 12px 0px;
}
</style>
