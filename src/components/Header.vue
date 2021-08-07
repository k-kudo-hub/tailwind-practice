<template>
  <section class="mx-auto bg-blue-300 h-16 flex justify-center items-center">
    <div class="sm:container flex h-20">
      <div class="w-1/4 h-20 flex justify-center items-center">
        <h1 class="text-4xl text-center text-white font-bold">
          <a href="/">
            {{ siteTitle }}
          </a>
        </h1>
      </div>
      <div class="w-1/2 flex">
        <SearchBar/>
      </div>
      <div class="w-1/4 flex">
        <PullDown/>
      </div>
    </div>
  </section>
</template>

<script>
import PullDown from './PullDown.vue'
import SearchBar from './SearchBar.vue'
import site from '../site-data.js'
export default {
  data(){
    return {
      siteTitle: site.TITLE
    }
  },
  components: {
    PullDown,
    SearchBar,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
