<template>
  <div class="FeaturedPost">

      <!-- image and content -->
    <HeroPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.featured"/>

    <!-- author -->
    <h2>FEATURED AUTHOR</h2>
    <div class="author container">
        <div class="avatar">
            <img :src="require('../../assets/img/source_images/' + post.author.image + '.jpg')" alt="post image">
        </div>
        <div class="info">
            <h3>{{ post.author.name }}</h3>
            <p>{{ post.author.bio }}</p>
        </div>
    </div>
  </div>
</template>

<script>
import HeroPost from './HeroPost.vue'

export default {
  name: 'FeaturedPost',
  components: {
    HeroPost
  },
  props: {
    posts: [],
    post: {}
  }
}
</script>

<style lang="scss">
@import "../../assets/style/common.scss";

.FeaturedPost {
    padding-top: 2rem;
    .author {
        margin-top: 1rem;
        justify-content: space-between;
        .avatar {
            width: 30%;
            img {
                width: 100%;
            }
        }
        .info {
            width: 65%;
            font-size: .7rem;
            p {
                margin-top: .5rem;
                color: #888888;
            }
        }
    }
}
</style>
