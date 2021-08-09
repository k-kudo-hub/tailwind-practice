<template>
  <div class="h-20 border-gray-100 border-b-2 flex items-center">
    <h2 class="w-1/6 text-xl font-bold pl-2">Projects</h2>
    <div class="w-3/6 h-1/2 flex items-center">
      <input type="text" class="border border-gray-300 py-1 px-3 rounded-3xl w-11/12 placeholder-gray-400" placeholder="Find a project...">
    </div>
    <div class="w-2/6 h-1/2 flex items-center">
      <select class="w-2/3 max-w-full border border-gray-300 py-1 px-3 rounded-3xl">
        <option value="Recently updated">Recently updated</option>
        <option value="Most stars">Most stars</option>
        <option value="Most forks">Most forks</option>
        <option value="Latest recently updated">Latest recently updated</option>
      </select>
    </div>
  </div>
  <div v-for="project in projects" :key="project.id" class="border-gray-100 border-b-2 flex display-col h-32 px-3 py-2">
    <div class="h-1/2 flex items-center w-full">
      <h2 class="w-1/2 font-bold text-md">{{ project.title }}</h2>
      <p class="w-1/2">Visit site </p>
    </div>
    <div class="h-1/2 flex items-center">
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      projects: [
        {
          title: "Tailwind Practice",
          stared: true,
          id: "tailwind-practice",
          language: "Vue.js",
          updated_at: "2h",
        },
        {
          title: "Vue3 Practice",
          stared: false,
          id: "vue3-practice",
          language: "Vue.js",
          updated_at: "4h",
        }
      ]
    }
  }
}
</script>

<style>

</style>
