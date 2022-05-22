<template>
  <div class="d-flex align-center">
    <v-avatar class="profile" color="grey" size="120" tile>
      <v-img src="/images/blog_pixs/related.jpg" class="rounded"></v-img>
    </v-avatar>

    <div class="mx-4">
      <span class="post__title">{{ postTitle }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "related-article",
  props: {
    postTitle: String,
  },
  data() {
    //
  },
};
</script>

<style scoped>
.post__title {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 500;
  font-size: 18px;
  line-height: 28px;
  color: #1e212b;
}
</style>
