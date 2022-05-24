<template>
  <v-container fluid class="pa-0">
    <div
      style="
        min-height: 50vh;
        position: relative;
        width: 100%;
        margin: 0px;

        background: #f1f0ea;
      "
    >
      <v-container>
        <v-row class="d-flex justify-center align-center">
          <v-col cols="12" md="5" offset-md="1">
            <div class="video-container py-16 px-8 px-md-0">
              <div
                class="video__player video-frame"
                style="background: #679436"
              ></div>
              <div class="video__player">
                <template>
                  <lite-youtube videoid="38iML94oi_c" class="youtube-lite" />
                </template>
              </div>
            </div>
          </v-col>
          <v-col cols="12" md="6">
            <div class="d-flex flex-column justify-start align-center pt-md-10">
              <h6
                class="section-title text-wrap px-4 text-center text-md-start pt-md-14"
              >
                {{ sectionTitle }}
              </h6>
              <p class="section-body py-8 py-md-7 px-4 px-md-14">
                {{ sectionBody }}
              </p>
              <div class="d-flex justify-md-start align-center mb-4 mb-md-1">
                <v-btn color="primary" outlined large class="section-btn left">
                  <span class="primary--text">
                    {{ button }}
                  </span>
                </v-btn>
              </div>
            </div>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </v-container>
</template>

<script>
export default {
  props: {
    sectionTitle: String,
    sectionBody: String,
    button: String,
  },
};
</script>

<style scoped>
.section-title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: bold;
  font-weight: 900;
  line-height: 53px;
  font-size: 36px;
  color: #1a1544;
}
.section-body {
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 20px;
  line-height: 28px;
  color: #1a1544;
}
.video__player {
  width: 100%;
  position: absolute;
  height: 300px;
  background-color: #ffffff;
  z-index: 1;
  border-radius: 25px;
}
.video-container {
  height: 400px;
  position: relative;
  /* z-index: 10; */
  justify-content: center;
  align-content: center;
}
.video-frame {
  width: 80%;
  height: 260px;
  margin-top: 80px;
  margin-left: -40px;
  border-radius: 25px;
}

.youtube-lite {
  width: 100%;
  height: 100%;
  border-radius: 25px;
}

@media only screen and (max-width: 768px) {
  .video-frame {
    display: none;
    margin: auto;
  }
  .video__player {
    border-radius: 4px;
  }
  .youtube-lite {
    width: 100%;
    height: 100%;
    border-radius: 4px;
  }
}
</style>
