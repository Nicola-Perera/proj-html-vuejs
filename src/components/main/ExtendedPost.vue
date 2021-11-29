<template>
    <div class="ExtendedPost">

      <!-- image -->
      <div class="post_image">
        <img :src="require('../../assets/img/source_images/' + post.image + '.jpg')" alt="post image">
      </div>

      <!-- content -->
      <div class="post_content container">
        <div class="post_date">
          <h3 class="day">{{ post.date.day }}</h3>
          <h3 class="month">{{ post.date.month }}</h3>
        </div>
        <div class="text">
          <h2 class="post_title">{{ post.title }}</h2>
          <p class="post_text">{{ post.text }}</p>
          <div class="info container">
            <div class="engage"></div>
            <div class="read_more"></div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>

export default {
  name: 'ExtendedPost',
  props: {
    post: {}
  }
}
</script>

<style lang="scss">
@import '../../assets/style/common.scss';

</style>
