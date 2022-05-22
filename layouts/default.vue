<template>
  <v-app>
    <app-header />
    <v-main style="background-color: #f7f5f5">
      <Nuxt />
    </v-main>
    <app-footer />
  </v-app>
</template>

<script>
import AppFooter from "../components/app-footer.vue";
import appHeader from "../components/app-header.vue";
export default {
  components: { appHeader, AppFooter },
  name: "DefaultLayout",
  data() {
    return {};
  },
};
</script>
