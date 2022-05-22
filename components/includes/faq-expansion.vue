<template>
  <div>
    <v-expansion-panels active-class="active">
      <v-expansion-panel>
        <v-expansion-panel-header class="faq__title">
          <template v-slot:actions>
            <v-icon dark color="primary">
              {{ isActive ? "mdi-minus-circle" : "mdi-plus-circle" }}
            </v-icon>
          </template>
          {{ title }}
        </v-expansion-panel-header>
        <v-expansion-panel-content class="answer">
          {{ answer }}
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </div>
</template>

<script>
export default {
  name: "faq-expansion",
  props: {
    title: String,
    answer: String,
  },

  data() {
    return {
      //,
    };
  },
};
</script>

<style scoped>
.v-expansion-panel {
  background-color: #ffffff;
  color: rgba(0, 0, 0, 0.87);
}
.active {
  background-color: #ffffff;
  color: rgba(0, 0, 0, 0.87);
  border-right: 16px #ddc8e3 solid;
}

.faq__title {
  font-style: normal;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-weight: 750;
  font-size: 18px;
  line-height: 29px;
  color: #1a1544;
  max-width: 35rem;
}
.faq__answer {
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  text-transform: capitalize;
  color: #4c4a59;
}
.v-expansion-panel:before {
  box-shadow: 0 5px 10px rgba(150, 160, 185, 0.05),
    0 15px 40px rgba(166, 173, 201, 0.2);
}
</style>
