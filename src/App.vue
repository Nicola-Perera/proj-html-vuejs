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
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'PHOTOGRAPY',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-46',
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
          id: '47',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'GADGETS',
          title: 'Gadgets that Make You Smartphone Even Smarter',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-47',
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
          id: '48',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'TRAVEL',
          title: '20 Top-Rated Tourist Attractions in Manhattan',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-48',
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
          id: '49',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'LIFESTYLE',
          title: 'The Best Way to Ride a Motorcycle',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-49',
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
          id: '50',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'TRAVEL',
          title: '5 Fun Things to Do at the Beach',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-50',
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
          id: '51',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-51',
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
          id: '55',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Simple Ways to Have a Pretty Face',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-55',
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '56',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-56',
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '57',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-57',
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '58',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-58',
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '59',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: 'John Doe',
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-59',
          status: {
            hero: false,
            popular: true,
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
