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
  }
}
</script>

<style>
/* @import './assets/style/common.scss'; */

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
