<template>
    <div id="SiteMain">

        <!-- hero posts -->
        <div class="hero_posts width80">
            <div class="width80">
                <HeroPost />
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
            <div v-for="genre in genres" class="genre" :class="genre.name" :key="genre.name">
                <button :name="genre.name"> {{ genre.name }} </button>
            </div>
        </div>

        <!-- main post contents -->
        <div class="main_content width80">

            <!-- width open posts -->
            <div class="extended_posts">
            </div>

            <!-- posts from social -->
            <div class="social_posts"></div>

        </div>
    </div>
</template>

<script>
import HeroPost from './HeroPost.vue'
import MiniPost from './MiniPost.vue'

export default {
  name: 'SiteMain',
  components: {
    HeroPost,
    MiniPost
  },
  data () {
    return {
      genres: [
        { name: 'GADGETS' },
        { name: 'PHOTOGRAPHY' },
        { name: 'LIFESTYLE' },
        { name: 'FASHION' },
        { name: 'RECIPES' },
        { name: 'TRAVEL' }
      ]
    }
  }
}

</script>

<style lang="scss">

</style>
