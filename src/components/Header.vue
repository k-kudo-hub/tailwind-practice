<template>
  <header class="sm:mx-auto bg-blue-300 h-16 flex justify-center items-center">
    <div class="sm:container flex h-16">
      <div class="w-1/4 h-16 flex justify-center items-center">
        <h1 class="sm:text-2xl md:text-3xl lg:text-4xl text-center text-white font-bold text-md">
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
  </header>
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
