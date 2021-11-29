<template>
  <div id="app">
    <SiteHeader :contacts="contacts" :nav="nav"/>
    <SiteMain :posts="posts" :genres="genres"/>
    <SiteFooter :posts="posts" :genres="genres" :categories="categories"/>

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
        { name: 'Gadgets' },
        { name: 'Photography' },
        { name: 'Lifestyle' },
        { name: 'Fashion' },
        { name: 'Recipes' },
        { name: 'Travel' }
      ],
      categories: [
        { name: 'Business' },
        { name: 'Architecture' },
        { name: 'Reviews' },
        { name: 'Sports' },
        { name: 'Videos' },
        { name: 'Technology' },
        { name: 'Design' }
      ],
      posts: [
        // hero posts
        {
          id: '46',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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

        // popular posts
        {
          id: '55',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
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
        },

        // main recent posts
        {
          id: '65',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Simple Ways to Have a Pretty Face',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-65',
          status: {
            hero: false,
            popular: false,
            recent: true,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '66',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-66 (1)',
          status: {
            hero: false,
            popular: false,
            recent: true,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '67',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-67',
          status: {
            hero: false,
            popular: false,
            recent: true,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '68',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-68',
          status: {
            hero: false,
            popular: false,
            recent: true,
            featured: false,
            extended: false,
            endpage: false
          }
        },
        {
          id: '69',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-69',
          status: {
            hero: false,
            popular: false,
            recent: true,
            featured: false,
            extended: false,
            endpage: false
          }
        },

        // featured posts
        {
          id: '66.1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar',
            bio: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam viverra euismod odio, gravida pelle, consectetur adipiscing elit.'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'blog-66',
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: true,
            extended: false,
            endpage: false
          }
        },

        // social posts
        // twitter
        {
          id: '1.2.3',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: true,
            instagram: false
          }
        },
        {
          id: '3.2.1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: true,
            instagram: false
          }
        },

        // instagram
        {
          id: '1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        {
          id: '2',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        {
          id: '3',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        {
          id: '4',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        {
          id: '5',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        {
          id: '6',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: '' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          },
          social: {
            twitter: false,
            instagram: true
          }
        },
        // extended posts
        {
          id: '54',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: 'blog-54' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          }
        },
        {
          id: '55.1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Simple Ways to Have a Pretty Face',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: 'blog-55 (1)' }
          ],
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          }
        },
        {
          id: '56.1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: 'blog-56 (1)' }
          ],
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          }
        },
        {
          id: '58.1',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: 'blog-58 (1)' }
          ],
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: true,
            endpage: false
          }
        },

        // top posts
        {
          id: '13.16.20.23.29.40',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'Recipes',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: [
            { name: 'blog-13' },
            { name: 'blog-16' },
            { name: 'blog-20' },
            { name: 'blog-23' },
            { name: 'blog-29' },
            { name: 'blog-40' }
          ],
          status: {
            hero: false,
            popular: true,
            recent: false,
            featured: false,
            extended: true,
            endpage: false,
            top10: true
          }
        },

        // footer posts
        {
          id: '04',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'our-office-4-square',
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: true
          }
        },
        {
          id: '05',
          date: {
            day: '12',
            month: 'January',
            year: '2019'
          },
          author: {
            name: 'John Doe',
            image: 'avatar'
          },
          genre: 'RECIPES',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          overview: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos.',
          text: 'Euismod atras vulputate iltricies etri elit. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Nulla nunc dui, tristique in semper vel, congue sed ligula. Nam dolor ligula, faucibus id sodales in, auctor fringilla libero. Pellentesque pellentesque tempor tellus eget hendreit. Morbi id aliquam ligula. Aliquam id dui sem. Proin rhoncus consequat nisl, eu ornare mauris tincidunt vitae. [...]',
          image: 'our-office-5-square',
          status: {
            hero: false,
            popular: false,
            recent: false,
            featured: false,
            extended: false,
            endpage: true
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
