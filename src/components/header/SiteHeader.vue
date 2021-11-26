<template>
    <div id="SiteHeader">

        <!-- general contacts -->
        <div class="header_top">
            <div class="contacts width80 container">
                <h3>Everything about Lifestyle, Travel and Gadgets!</h3>
                <div v-for="link in contacts" :key="link.name"><a class="link" href="#">{{ link.name }}</a></div>
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
  props: {
    nav: [],
    contacts: []
  }
}

</script>

<style lang="scss">
@import '../../assets/style/common.scss';

#SiteHeader {
    .header_top {
        padding: 1rem 0;
        font-size: .6rem;
        background-color: #0088cc;
        color: #fff;
        h3 {
            font-weight: 200;
        }
        a {
            margin-left: 1rem;
            font-weight: bold;
            color: #fff;
        }
    }
    #header_logo {
        padding: 2rem 0;
        img {
            width: 5rem;
            }
    }
}

.header_bottom {
    border-top: 2px solid #ededed;
}

</style>
