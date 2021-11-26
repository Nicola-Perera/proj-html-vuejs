<template>
    <div id="SiteMain">

        <!-- hero posts -->
        <div class="hero_posts">
            <div class="width80 container">
                <HeroPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.hero"/>
            </div>
        </div>

        <!-- post overview -->
        <div class="post_overview width80">

            <!-- popular posts -->
            <div class="popular_posts">
                <h2>POPULAR POSTS</h2>
                <MiniPost />
            </div>

            <!-- recent posts -->
            <div class="recent_posts">
                <h2>RECENT POSTS</h2>
                <MiniPost />
            </div>

            <!-- featured posts -->
            <div class="featured_posts">
                <h2>FEATURED POSTS</h2>
            </div>

        </div>

        <!-- genres -->
        <div class="genres">
            <div class="width80">
                <div v-for="genre in genres" class="genre" :class="genre.name" :key="genre.name">
                    <button :name="genre.name"> {{ genre.name }} </button>
                </div>
            </div>
        </div>

        <!-- main post contents -->
        <div class="main_content width80">

            <!-- width open posts -->
            <div class="extended_posts">
                <ExtendedPost />
            </div>

            <!-- posts from social -->
            <div class="social_posts"></div>

        </div>
    </div>
</template>

<script>
import HeroPost from './HeroPost.vue'
import MiniPost from './MiniPost.vue'
import ExtendedPost from './ExtendedPost.vue'

export default {
  name: 'SiteMain',
  props: {
    genres: [],
    posts: [],
    post: {}
  },
  components: {
    HeroPost,
    MiniPost,
    ExtendedPost
  }
}

</script>

<style lang="scss">
@import '../../assets/style/common.scss';

.hero_posts {
    background-color: #f7f7f7;
    padding: 2.5rem 0;
    .width80.container {
        flex-wrap: wrap;
        justify-content: space-between;
        #HeroPost {
            width: calc(100% / 3.1);
        }
    }
}

</style>
