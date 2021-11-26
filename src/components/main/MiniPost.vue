<template>
    <div id="MiniPost">
      <div class="container">
        <div class="post_image">
          <img :src="require('../../assets/img/source_images/' + post.image + '.jpg')" alt="">
        </div>
        <div class="post_content">
          <h3>{{ post.title }}</h3>
          <h4><span>{{ post.date.month }}</span> <span>{{ post.date.day }}</span>, <span>{{ post.date.year }}</span></h4>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'MiniPost',
  props: {
    post: {}
  }
}
</script>

<style lang="scss">
@import '../../assets/style/common.scss';

#MiniPost {
  .post_image {
    width: 3rem;
    img {
      width: 100%;
    }
  }
}

</style>
