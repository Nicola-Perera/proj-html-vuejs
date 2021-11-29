<template>
    <div class="SocialPost">
        <div class="container">
            <div class="social_logo"></div>
            <div class="contnet">
                <p class="text">{{ post.text }}</p>
                <p class="date"><span>{{ post.date.month }}</span> <span>{{ post.date.day }}</span>, <span>{{ post.date.year }}</span></p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'SocialPost',
  props: {
    post: {}
  }
}
</script>

<style lang="scss">
@import '../../assets/style/common.scss';

.SocialPost {
    .container {
        .cotent {
            .date {
                color: #0088cc;
            }
        }
    }
}

</style>
