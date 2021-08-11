<template>
  <Loading v-show="loading"/>
  <div class="h-content sm:flex">
    <aside class="sm:w-1/4 min-h-full bg-gray-50 py-0 sm:py-5 px-2 w-full">
      <SelfIntroduce/>
    </aside>
    <section class="sm:w-3/4 min-h-full bg-white py-5 px-2 w-full">
      <ProjectList/>
    </section>
  </div>
</template>

<script>
import SelfIntroduce from './SelfIntroduce.vue'
import ProjectList from './ProjectList.vue'
import Loading from './Loading.vue'
export default {
  data(){
    return {
      isOpen: false,
      loading: true,
    }
  },
  mounted() {
    // -- Some processing -- //
    this.loading = false;
  },
  components: {
    SelfIntroduce,
    ProjectList,
    Loading,
  },
  methods: {
    toggleOpen(){
      this.isOpen ? this.isOpen = false : this.isOpen = true;
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
.h-content {
  min-height: calc(100vh - 64px - 136px)
}
</style>
