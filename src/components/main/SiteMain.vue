<template>
    <div class="SiteMain">

        <!-- hero posts -->
        <div class="hero_posts">
            <div class="width80 container">
                <HeroPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.hero"/>
            </div>
        </div>

        <!-- post overview -->
        <div class="post_overview width80 container">

            <!-- popular posts -->
            <div class="popular_posts">
                <h2>POPULAR POSTS</h2>
                <MiniPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.popular"/>
            </div>

            <!-- recent posts -->
            <div class="recent_posts">
                <h2>RECENT POSTS</h2>
                <MiniPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.recent"/>
            </div>

            <!-- featured posts -->
            <div class="featured_posts">
                <h2>FEATURED POSTS</h2>
            </div>

        </div>

        <!-- genres -->
        <div class="genres">
            <div class="width80 container">
                <div class="arrow left"><span>&lArr;</span></div>
                <div v-for="genre in genres" class="genre" :class="genre.name" :key="genre.name">
                    <h2> {{ genre.name }} </h2>
                </div>
                <div class="arrow rigth"><span>&rArr;</span></div>
            </div>
        </div>

        <!-- main post contents -->
        <div class="main_content width80">

            <!-- width open posts -->
            <div class="extended_posts">
                <ExtendedPost v-for="post in posts" :post="post" :posts="posts" :key="post.id" v-show="post.status.extended"/>/>
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
.SiteMain {

    // hero posts
    .hero_posts {
        background-color: #f7f7f7;
        padding: 2.5rem 0;
        .width80.container {
            flex-wrap: wrap;
            justify-content: space-between;
            .HeroPost {
                width: calc(100% / 3.1);
            }
        }
    }

    // mini posts
    .post_overview {
        justify-content: space-between;
        .popular_posts, .recent_posts, .featured_posts {
            width: calc(100% / 3.1);
        //  h2 {
        //         font-size: .5rem;
        //     }
        }
        .popular_posts {
            h2 {
                font-size: .8rem;
                margin-top: 2rem;
            }
        }
        .recent_posts {
            h2 {
                font-size: .8rem;
                margin-top: 2rem;
            }
        }
    }

    // lista generi
    .genres {
        background-color: #0088cc;
        .width80.container {
            justify-content: space-between;
            align-items: center;
        }
        .genre {
            padding: 2rem 0;
            h2 {
                color: white;
                background-color: #212529;
                padding: 1rem 3rem;
                font-size: .6rem;
            }
        }
    }
}

</style>
