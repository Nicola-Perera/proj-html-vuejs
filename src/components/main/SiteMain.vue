<template>
    <div id="SiteMain">

        <!-- genres -->
        <div class="genres">
            <div v-for="genre in genres" class="genre" :class="genre.name" :key="genre.name">
                <button :name="genre.name"> {{ genre.name }} </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'SiteMain',
  components: {

  },
  data () {
    return {
      genres: [
        { name: 'GADGETS' },
        { name: 'PHOTOGRAPHY' },
        { name: 'LIFESTYLE' },
        { name: 'FASHION' },
        { name: 'RECIPES' },
        { name: 'TRAVEL' }
      ]
    }
  }
}

</script>

<style lang="scss">

</style>
