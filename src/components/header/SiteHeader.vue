<template>
    <div id="SiteHeader">

        <!-- general contacts -->
        <div class="header_top">
            <div class="contacts width80">
                <h3>Everything about Lifestyle, Travel and Gadgets!</h3>
                <div v-for="link in contacts" :key="link.name"><a href="#">{{ link.name }}</a></div>
            </div>
        </div>

        <!-- logo -->
        <div id="header_logo" class="width80">
            <img src="../../assets/img/source_images/logo-default-slim.png" alt="">
        </div>

        <!-- navbar -->
        <div class="header_bottom">
            <div class="nav width80">
                <div v-for="link in nav" :key="link.name"><a href="#">{{ link.name }}</a></div>
            </div>
        </div>

    </div>
</template>

<script>
export default {
  name: 'SiteHeader',
  components: {

  },
  data () {
    return {
      nav: [{ name: 'Home' }, { name: 'Element' }, { name: 'Features' }, { name: 'Pages' }, { name: 'Portfolio' }, { name: 'Blog' }, { name: 'Shop' }],
      contacts: [{ name: 'SIGN IN' }, { name: 'ABOUT US' }, { name: 'CONTACT US' }, { name: 'BUY NOW' }]
    }
  }
}

</script>

<style>
img {
    width: 5rem;
    }

.header_bottom {
    border-top: 2px solid #ededed;
}

</style>
