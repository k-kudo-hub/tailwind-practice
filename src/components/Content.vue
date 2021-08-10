<template>
  <div class="h-content flex">
    <aside class="sm:w-1/4 min-h-full bg-gray-50 py-5 px-2 hidden sm:block">
      <SelfIntroduce/>
    </aside>
    <section class="sm:w-3/4 min-h-full bg-white py-5 px-2 w-full">
      <ProjectList/>
      <button>
        click here
      </button>
    </section>
  </div>
</template>

<script>
import SelfIntroduce from './SelfIntroduce.vue'
import ProjectList from './ProjectList.vue'
export default {
  data(){
    return {
      
    }
  },
  components: {
    SelfIntroduce,
    ProjectList,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
.h-content {
  min-height: calc(100vh - 64px - 136px)
}
</style>
