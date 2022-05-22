<template>
  <v-container>
    <v-row>
      <v-col cols="12" md="9">
        <div class="px-2 px-md-10 section__container">
          <h6 class="post__title">{{ post.post_title }}</h6>
          <p class="author">
            by <span>{{ post.author }}</span> {{ post.created_at }}
          </p>
          <v-img class="post__image" height="430" :src="post.image_src">
          </v-img>
          <p class="post__content">{{ post.content }}</p>
          <p class="post__content">{{ post.content }}</p>
          <p class="post__content">{{ post.content }}</p>
          <div class="d-block d-md-flex align-center my-8 mt-md-13 pb-12">
            <span class="font-weight-bold pr-2"> Tags: </span>
            <v-chip-group active-class="primary--text" column>
              <v-chip
                color="white"
                class="chips"
                v-for="tag in tags"
                :key="tag"
              >
                {{ tag }}
              </v-chip>
            </v-chip-group>
            <v-spacer></v-spacer>
            <span
              class="primary--text text-decoration-underline font-weight-bold pr-md-8"
              >comments({{ post.comments }})</span
            >
          </div>
        </div>
        <div class="section__container mb-8" style="max-width: 756px">
          <div class="pt-5 pb-7 px-5">
            <span class="author__header pt-5 px-3">About author</span>
          </div>
          <div class="d-flex align-center pa-0 ma-0">
            <v-avatar class="ml-7 mr-4 mb-5 align-self-start" size="52">
              <img alt="Avatar" :src="post.author_avatar" />
            </v-avatar>

            <div>
              <div>
                <span class="author__header">{{ post.author }}</span>
              </div>
              <div class="pb-4 pr-2">
                <span class="author__desc">
                  {{ post.author_desc }}
                </span>
              </div>
            </div>
          </div>
        </div>
        <div class="comment__section">
          <div class="comment__section__title">
            <p class="text-capitalize author__header">leave a reply</p>
            <span
              >Your email address will not be published. Required fields are
              marked*</span
            >
          </div>
          <div class="form__inputs">
            <blog-comments />
          </div>
        </div>
      </v-col>
      <v-col cols="12" md="3" v-if="$vuetify.breakpoint.mdAndUp">
        <div class="section__container">
          <h6 class="author__header px-auto pl-md-6 py-6">Related Articles</h6>
          <div v-for="item in 5" :key="item">
            <related-articles
              :postTitle="post.post_title"
              class="py-md-4 px-2 px-md-6"
            />
          </div>
          <div class="d-flex flex-column justify-center px-6 pb-md-13">
            <span class="font-weight-bold py-10"> Tag:</span>
            <v-chip-group active-class="primary--text" column>
              <v-chip
                color="white"
                class="chips"
                v-for="tag in tags"
                :key="tag"
              >
                {{ tag }}
              </v-chip>
            </v-chip-group>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import blogComments from "../../../components/includes/blog-comments.vue";
import RelatedArticles from "../../../components/includes/related-articles.vue";
export default {
  components: { blogComments, RelatedArticles },
  name: "single-post",
  data() {
    return {
      post: {
        post_title: "Choosing Plants for Water Conservation",
        author: "John Doe",
        author_avatar: "https://i.pravatar.cc/300",
        author_desc:
          "Arcu placerat integer integer in. Ultrices morbi nullam purus ultrices venenatis rutrum tortor",
        created_at: "04 Jun 2021",
        image_src: "/images/gallery/pix7.jpg",
        content:
          "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ultricies ut magna enim donec. Orci pulvinar sodales nec mattis. Sed lorem tellus volutpat massa. Laoreet neque, sed quis nam viverra vel in cursus. Duis urna semper posuere eget dictum vestibulum hac phasellus. Vel tristique quis eu hendrerit massa facilisis et. Sit elit orci quis malesuada massa sed sit tincidunt non. Enim porttitor eget donec cras. Cras proin arcu enim sit congue pulvinar proin tristique mattis. A sit placerat purus fusce",
        comments: 12,
      },
      tags: ["Work", "Home Improvement", "Vacation", "Food"],

      comments: [],
    };
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Nunito+Sans&display=swap");

.section__container {
  margin-top: 64px;
  background: #ffffff;
  border-radius: 20px;
}

.post__title {
  padding-top: 30px;
  padding-bottom: 8px;
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 750;
  font-size: 36px;
  line-height: 43px;
  color: #1e212b;
}
.author {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #4a4a4a;
}
.author span {
  font-family: "Segoe UI", Tahoma, "Geneva", Verdana, sans-serif;
  font-style: normal;
  font-weight: 600;
  font-size: 18px;
  line-height: 22px;
  color: #4a4a4a;
}
.post__image {
  margin-top: 39px;
}

.post__content {
  padding-top: 48px;
  font-family: "Nunito Sans", sans-serif;
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 28px;
  color: #4c5158;
}
.chips {
  background-color: #ffffff;
  box-shadow: 0px 4px 7px rgba(0, 0, 0, 0.07);
}

.author__header {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 600;
  font-size: 22px;
  line-height: 28px;
  color: #1e212b;
}

.author__desc {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 18px;
  line-height: 22px;
  color: #1e212b;
}

.comment__section {
  margin-top: 64px;
  padding-left: 30px;
  padding-right: 80px;
  margin-bottom: 260px;
  max-width: 840px;
  background: #f0eded;
  border-radius: 20px;
}
.comment__section__title {
  padding-top: 38px;
  padding-bottom: 38px;
}
.comment__section__title span {
  font-family: "Roboto";
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 17px;
  color: #908daa;
}

@media only screen and (max-width: 768px) {
  /* For mobile phones: */
  .section__container {
    margin-top: 32px;
  }
  .post__title {
    padding-top: 30px;
    padding-bottom: 8px;
    font-weight: 750;
    font-size: 24px;
    line-height: 24px;
  }
  .author {
    font-size: 14px;
    line-height: 12px;
  }
  .author span {
    font-size: 14px;
    line-height: 12px;
  }
  .post__content {
    padding-top: 18px;
    font-weight: 400;
    font-size: 18px;
    line-height: 22px;
  }
  .author__desc {
    font-size: 12px;
    line-height: 8px;
  }
  .comment__section {
    margin-top: 32px;
    padding-left: 16px;
    padding-right: 16px;
    margin-bottom: 32px;
  }
}
</style>
