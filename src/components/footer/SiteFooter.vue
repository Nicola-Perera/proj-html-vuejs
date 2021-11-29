<template>
    <div class="SiteFooter">
      <div class="width80 container">

        <!-- info about the blog -->
        <div class="about">
          <h3>ABOUT THE BLOG</h3>
          <p>Lorem ipsum sit amet, consectetur adipiscing elit. Donec eu pulvinar magna semper scelerisque.</p>
          <p>Proesent venenatis turpis vitae purus semper, eget sogittis velit venenatis ptent taciti sociosqu ad litora...</p>
          <h3>VIEW MORE &rArr;</h3>
        </div>

        <!-- most recent posts -->
        <div class="most_recent_posts">
          <h3>RECENT POSTS</h3>
          <MiniPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.endpage"/>
        </div>

        <!-- most recent comments -->
        <div class="most_recent_comments">
          <h3>RECENT Comments</h3>
        </div>

        <!-- categories -->
        <div class="categories">
          <h3>CATEGORIES</h3>
        </div>
      </div>
    </div>
</template>

<script>
import MiniPost from '../main/MiniPost.vue'

export default {
  name: 'SiteFooter',
  props: {
    genres: [],
    posts: [],
    post: {}
  },
  components: {
    MiniPost
  }
}

</script>

<style lang="scss">
@import '../../assets/style/common.scss';

.SiteFooter {
  // common rules
  background-color: var(--theme-dark-grey);
  font-size: .6rem;
  .width80 {
    padding-top: 4rem;
    padding-bottom: 6rem;
  }
  h3 {
    color: white;
  }
  p {
    color: #888888;
    margin-top: 1rem;
    margin-bottom: .6rem;
  }
  .about, .most_recent_posts, .most_recent_comments, .categories {
    width: calc(100% / 4);
  }

  // posts
  .most_recent_posts {
    .MiniPost {
      border-bottom: initial;
      .post_image {
        width: 5rem;
        img {
          border-radius: 2rem;
        }
      }
      .post_content {
        font-size: .7rem;
        h3 {
          color: #b7b7b7;
        }
        h4 {
          color: #888888;
        }
      }
    }
  }
}

</style>
