<template>
  <div id="app">
    <SiteHeader :contacts="contacts" :nav="nav"/>
    <SiteMain :posts="posts" :genres="genres"/>
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
      nav: [{ name: 'HOME' }, { name: 'ELEMENT' }, { name: 'FEATURES' }, { name: 'PAGES' }, { name: 'PORTOFOLIO' }, { name: 'BLOG' }, { name: 'SHOP' }],
      contacts: [{ name: 'SIGN IN' }, { name: 'ABOUT US' }, { name: 'CONTACT US' }, { name: 'BUY NOW' }],
      genres: [
        { name: 'GADGETS' },
        { name: 'PHOTOGRAPHY' },
        { name: 'LIFESTYLE' },
        { name: 'FASHION' },
        { name: 'RECIPES' },
        { name: 'TRAVEL' }
      ],
      posts: [
        {
          id: '46',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '45',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '44',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '43',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '42',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '41',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46.jpg',
          status: {
            hero: true,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        }
      ]
    }
  }
}
</script>

<style lang='scss'>
@import './assets/style/common.scss';

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
}
</style>
