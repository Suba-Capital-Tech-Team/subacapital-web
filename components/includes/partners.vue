<template>
  <v-container>
    <h5 class="partners text-center pt-4 pt-md-16 mt-md-14 pb-2 pb-md-8">
      Featured On
    </h5>
    <div class="partners-container partners flex-wrap">
      <img src="/images/partners/leadway.png" alt="LEADWAY ASSURANCE" />
      <img src="/images/partners/fmn.png" alt="FMN" />
      <img src="/images/partners/usaid.png" alt="USAID TRADE HUB" />
      <img src="/images/partners/afex.png" alt="AFEX" />
      <img src="/images/partners/fcmb.png" alt="FCMB" />
    </div>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.partners-container {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 18px;
  margin: 50px 5px;
}

img {
  max-width: 50px;
  display: inline-flex;
}
.partners {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: bold;
  font-weight: 750;
  font-size: 36px;
  line-height: 53px;
  text-transform: capitalize;
}

@media screen and (min-width: 480px) {
  .partners {
    gap: 50px;
    margin: 80px 5px;
  }
}

@media screen and (min-width: 600px) {
  .partners {
    gap: 80px;
    margin: 100px 5px;
  }
  img {
    max-width: 120px;
  }
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .partners {
    font-size: 26px;
    text-transform: capitalize;
  }
}
</style>
