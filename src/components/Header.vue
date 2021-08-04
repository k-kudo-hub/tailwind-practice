<template>
  <section class="mx-auto bg-blue-300 h-20 flex justify-center items-center">
    <div class="sm:container flex h-20">
      <div class="w-1/3 h-20 flex justify-center items-center">
        <h1 class="text-4xl text-center text-white font-bold">Tailwind</h1>
      </div>
      <div class="w-2/3 flex">
        <PullDown/>
      </div>
    </div>
  </section>
</template>

<script>
import PullDown from './PullDown.vue'
export default {
  components: {
    PullDown,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
