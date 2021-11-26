<template>
    <div id="HeroPost">
      <div class="hero_image">
        <img :src="require('../../assets/img/source_images/' + post.image + '.jpg')" alt="">
        <div class="hero_content">
            <h3 class="genre">{{ post.genre }}</h3>
          <p>{{ post.title }}</p>
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

#HeroPost {
  // color: #fff;
  .hero_image {
    img {
      width: 100%;
    }
    .hero_content {
        h3 {
          padding: .5rem 1rem;
          display: inline-block;
          background-color: #0088cc;
        }
    }
  }
}

</style>
