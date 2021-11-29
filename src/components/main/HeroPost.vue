<template>
    <div class="HeroPost">
      <div class="hero_image">
        <img :src="require('../../assets/img/source_images/' + post.image + '.jpg')" alt="post image">
        <div class="hero_content">
          <div class="genre_bg">
            <h3 class="genre"><span>{{ post.genre.toUpperCase() }}</span></h3>
          </div>
          <p>{{ post.title }}</p>
          <p class="overview">{{ post.overview }}</p>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'HeroPost',
  props: {
    post: {}
  }
}
</script>

<style lang="scss">
@import '../../assets/style/common.scss';

.HeroPost {
  .hero_image {
    position: relative;
    color: white;
    font-weight: bold;
    img {
      width: 100%;
    }
    .hero_content {
      position: absolute;
      bottom: 0;
      left: 0;
      padding: 1rem;
      &:hover .overview{
        display: block;
      }
      .genre_bg {
        h3 {
          padding: .2rem .5rem;
          display: inline-block;
          background-color: var(--theme-green);
          font-size: .5rem;
          span {
            padding: .05rem .49rem;
          }
          &:hover span {
            background-color: var(--theme-grey);
          }
        }
      }
      p {
        margin-top: .3rem;
        font-size: .9rem;
      }
      .overview {
        display: none;
        color: #b7b7b7;
      }
    }
  }
}

</style>
