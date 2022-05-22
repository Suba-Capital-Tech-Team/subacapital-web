<template>
  <div>
    <form action="">
      <v-row class="d-flex justify-center align-center">
        <v-col cols="12" md="6" class="mx-0">
          <v-text-field
            hide-details="auto"
            background-color="#F5F7FA"
            v-model="comment.name"
            rounded
            label="Name*"
            filled
          ></v-text-field>
        </v-col>
        <v-col cols="12" md="6" class="mx-0">
          <v-text-field
            hide-details="auto"
            background-color="#F5F7FA"
            v-model="comment.email"
            rounded
            label="Email*"
            filled
          ></v-text-field>
        </v-col>
     
        <v-col cols="12" class="mx-0">
          <v-textarea
            hide-details="auto"
            background-color="#F5F7FA"
            v-model="comment.message"
            rounded
            label="comment"
            filled
          ></v-textarea>
        </v-col>
        <v-col cols="12" class="mx-0">
          <v-btn color="primary" dark x-large class="px-11 mb-4 mb-md-7 text-capitalize">
            comment
          </v-btn>
        </v-col>
      </v-row>
    </form>
  </div>
</template>

<script>
export default {
    name: "comments",
    data(){
        return {
            comment: {
                name: "",
                email: "",
                message: ""
            }
        }
    }
};
</script>

<style scoped></style>
