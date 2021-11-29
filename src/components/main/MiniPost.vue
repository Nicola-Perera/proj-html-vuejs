<template>
    <div class="MiniPost">
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

.MiniPost {
  margin-top: .9rem;
  padding-bottom: .4rem;
  border-bottom: 1px solid #e2e2e2;
  .post_image {
    width: 3rem;
    min-height: 3.5rem;
    margin-right: 1rem;
    img {
      width: 100%;
    }
  }
  .post_content {
    font-size: .7rem;
    h3 {
      color: #888888;
    }
    h4 {
      color: #b7b7b7;
    }
  }
}

</style>
