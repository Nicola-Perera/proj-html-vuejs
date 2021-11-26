<template>
    <div id="HeroPost">
      <h3>{{ post.id }}</h3>
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

</style>
