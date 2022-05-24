<template>
  <div style="height: 340px; width: 100%">
    <v-card
    flat
    :rounded="$vuetify.breakpoint.mdAndUp"
    class="mx-2 rounded-sm"
    height="100%"
    :width="cardWidth[$vuetify.breakpoint.name]"
  >
    <div class="card-message px-5 pt-14">{{ message }}</div>
    <div class="customer-details-container d-flex align-center py-8">
      <v-avatar class="ml-5 mr-1 align-self-start" size="44">
        <img alt="Avatar" :src="avatar" />
      </v-avatar>
      <div class="d-flex flex-column justify-end align-start">
        <h6 class="client">{{ client }}</h6>
        <p class="title">{{ title }}</p>
      </div>
    </div>
  </v-card>
  </div>
</template>

<script>
export default {
  name: "slide-cards",
  props: {
    avatar: String,
    client: String,
    title: String,
    message: String,
  },
  data() {
    return {
      cardWidth: {
        xs: "320px",

        md: "355px",
      },
    };
  },
};
</script>

<style scoped>
.client {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 20px;
  line-height: 24px;
  text-transform: capitalize;
  color: rgba(33, 26, 85, 1);
}
.title {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-size: 0.9rem !important;
  font-weight: 400;
  line-height: 1.5rem;
  letter-spacing: 0.03125em !important;
  color: #908daa;
}
.card-message {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #908daa;
}
</style>
