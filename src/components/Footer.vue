<template>
  <footer class="mx-auto bg-indigo-700 min-h-40">
    <div class="mx-auto py-4 px-5 flex flex-col sm:flex-row max-w-3xl">
      <div class="sm:w-1/2 flex flex-col sm:mx-auto sm:text-left mb-2">
        <h2 class="text-white text-3xl">{{ siteTitle }}</h2>
        <p class="text-white">{{ subTitle }}</p>
      </div>
      <div class="sm:w-1/2 flex mx-auto w-11/12 sm:w-full">
        <div class="w-1/2">
          <p class="text-white sm:text-center">SNS</p>
          <ul class="text-gray-300 mt-2 sm:ml-20">
            <li><a href="" class="hover:text-white">Facebook</a></li>
            <li><a href="" class="hover:text-white">Twitter</a></li>
            <li><a href="" class="hover:text-white">Instagram</a></li>
          </ul>
        </div>
        <div class="w-1/2">
          <p class="text-white sm:text-center">Tailwind</p>
          <ul class="text-gray-300 mt-2 sm:ml-20">
            <li><a href="#" class="hover:text-white">blog</a></li>
            <li><a href="#" class="hover:text-white">components</a></li>
            <li><a href="#" class="hover:text-white">cheets sheet</a></li>
          </ul>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import site from '../site-data.js'
export default {
  data(){
    return {
      siteTitle: site.TITLE,
      subTitle: site.SUB_TITLE
    }
  }
}
</script>

<style scoped>

</style>
