<template>
    <div id="MiniPost">
      <h3>{{ post.genre }}</h3>
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

</style>
