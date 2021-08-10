<template>
  <div class="h-content flex">
    <aside class="w-1/4 min-h-full bg-gray-50 py-5 px-2">
      <SelfIntroduce/>
    </aside>
    <section class="w-3/4 min-h-full bg-white py-5 px-2">
      <ProjectList/>
    </section>
  </div>
</template>

<script>
import SelfIntroduce from './SelfIntroduce.vue'
import ProjectList from './ProjectList.vue'
export default {
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
