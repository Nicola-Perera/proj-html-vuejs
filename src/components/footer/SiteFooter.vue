<template>
    <div class="SiteFooter">

      <!-- top footer -->
      <div class="footer_top">
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
            <h3>RECENT COMMENTS</h3>
            <div class="comment" v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.endpage">
              <h3><span class="author">{{ post.author.name }}</span> commented on <span class="post">lorem ipsum dolor sit amet.</span></h3>
              <h4><span>{{ post.date.month }}</span> <span>{{ post.date.day }}</span>, <span>{{ post.date.year }}</span></h4>
            </div>
          </div>

          <!-- all categories -->
          <div class="categories">
            <h3>CATEGORIES</h3>
            <div class="all_categories container">
              <!-- genres -->
              <div v-for="genre in genres" class="genre categories" :class="genre.name" :key="genre.name">
                <h2> {{ genre.name.toUpperCase() }} </h2>
              </div>
              <!-- categories -->
              <div v-for="category in categories" class="category categories" :class="category.name" :key="category.name">
                      <h2> {{ category.name.toUpperCase() }} </h2>
                  </div>
            </div>
          </div>
        </div>
      </div>

      <!-- bottom footer -->
      <div class="footer_bottom">
        <div class="width80 container">

          <!-- copyright -->
          <div class="credits container">
            <div class="logo">
              <img src="../../assets/img/source_images/logo-footer.png" alt="page logo grey">
            </div>
            <div class="copyright">
              <h4>&copy; Copyright 2020, All Rights Reserved</h4>
            </div>
          </div>

          <!-- contacts -->
          <div class="contatcs container">
            <h4>&rArr; FAQ's</h4>
            <h4>&rArr; Sitemap</h4>
            <h4>&rArr; Contact Us</h4>
          </div>
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
    categories: [],
    posts: []
  },
  components: {
    MiniPost
  }
}

</script>

<style lang="scss">
@import '../../assets/style/common.scss';

// top section
.footer_top {
  // common rules
  background-color: var(--theme-grey);
  font-size: .6rem;
  padding-top: 4rem;
  padding-bottom: 6rem;
  .container {
    justify-content: space-between;
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
    width: calc(100% / 4.3);
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

  // comments
  .comment {
    margin-top: .5rem;
    h3 {
      color: #b7b7b7;
        .author {
          color: white;
        }
        .post {
          color: #0074ad;
        }
    }
    h4 {
      color: #888888;
    }
  }

  // categories
  .all_categories {
    color: white;
    flex-wrap: wrap;
    padding-top: 1rem;
    .categories {
      background-color: black;
      font-size: .4rem;
      padding: .3rem;
      margin-right: .4rem;
      margin-bottom: .2rem;
      border-radius: .2rem;
      h2 {
        width: 100%;
      }
    }
  }
}

// bottom section
.footer_bottom {
  background-color: var(--theme-dark-grey);
  font-size: .6rem;
  padding: 1rem;
  .width80.container {
    justify-content: space-between;
    align-items: center;
    h4 {
      color: #555555;
    }
    .credits {
      width: 30%;
      align-items: center;
      .logo {
        width: 30%;
        img {
          width: 80%;
        }
      }
      .copyright {
        width: 70%;
      }
    }

    // contacts
    .contacts {
      width: 30%;
    }
  }
}

</style>
