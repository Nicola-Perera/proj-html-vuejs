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
            <h3 class="month">{{ post.date.month.substring(0,3).toUpperCase() }}</h3>
        </div>
        <div class="text">
          <h2 class="post_title">{{ post.title }}</h2>
          <p class="post_text">{{ post.text }}</p>
          <div class="info container">
            <div class="engage">
              <p>By <span>{{ post.author.name }}</span> <span>{{ post.genre }}</span> <span>12 Comments</span></p>
            </div>
            <div class="read_more">
              <button>READ MORE</button>
            </div>
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

.ExtendedPost {
  margin: 3rem 0;
  .post_image {
    width: 100%;
    img {
      width: 100%;
    }
  }
  .post_content {
    margin: 2rem 0;
    justify-content: space-between;

    .post_date {
      font-size: .8rem;
      text-align: center;
      width: 5%;
      .day {
        background-color: #f7f7f7;
        padding: 1rem;
      }
      .month {
        background-color: #212529;
        color: white;
        padding: .3rem .5rem;
      }
    }
    .text {
      width: 93%;
      padding-bottom: 1rem;
      border-bottom: 2px solid #eeeeee;
      padding: 0 .5rem;
      p {
        margin: 1rem 0;
        color: #888888;
      }
      .info {
        justify-content: space-between;
         .engage {
          p {
            span {
              margin-right: .5rem;
              color: #0088cc;
            }
          }
        }
        button {
          color: #888888;
          background-color: transparent;
          border: 2p solid #eeeeee;
          border-radius: .2rem;
          padding: .3rem;
        }
      }
    }
  }
}
</style>
