<template>
  <section class="h-content flex">
    <div class="w-1/4 min-h-full bg-gray-50 py-5 px-2">
      <Selfintroduce/>
    </div>
    <div class="w-1/2 min-h-full bg-white py-5 px-2">
      <ProjectList/>
    </div>
    <div class="w-1/4 min-h-full bg-gray-50 py-5 px-2">
      <ActivityLog/>
    </div>
  </section>
</template>

<script>
import SelfIntroduce from './SelfIntroduce.vue'
import ProjectList from './ProjectList.vue'
import ActivityLog from './ActivityLog.vue'
export default {
  components: {
    SelfIntroduce,
    ProjectList,
    ActivityLog,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
.h-content {
  min-height: calc(100vh - 64px - 160px)
}
</style>
