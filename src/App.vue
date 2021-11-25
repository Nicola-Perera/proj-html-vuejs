<template>
  <div id="app">
    <SiteHeader />
    <SiteMain />
    <SiteFooter />

  </div>
</template>

<script>
import SiteHeader from './components/header/SiteHeader.vue'
import SiteMain from './components/main/SiteMain.vue'
import SiteFooter from './components/footer/SiteFooter.vue'

export default {
  name: 'App',
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter
  },
  data () {
    return {
      posts: [
        {
          id: '46',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          image: 'blog-46.jpg'
        }]
    }
  }
}
</script>

<style>
/* @import './assets/style/common.scss'; */

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
