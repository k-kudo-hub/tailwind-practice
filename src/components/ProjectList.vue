<template>
  <header class="h-20 border-gray-100 border-b-2 sm:flex items-center">
    <h1 class="sm:w-1/6 sm:mb-0 mb-1 text-xl font-bold pl-2">Projects</h1>
    <div class="flex sm:w-5/6">
      <div class="w-3/5 h-1/2 flex items-center">
        <input type="text" class="border border-gray-300 py-1 px-3 rounded-3xl w-11/12 placeholder-gray-400" placeholder="Find a project...">
      </div>
      <div class="w-2/5 h-1/2 flex items-center">
        <select class="sm:w-2/3 max-w-full border border-gray-300 py-1 px-3 rounded-3xl">
          <option value="Recently updated">Recently updated</option>
          <option value="Most stars">Most stars</option>
          <option value="Most forks">Most forks</option>
          <option value="Latest recently updated">Latest recently updated</option>
        </select>
      </div>
    </div>
  </header>
  <article v-for="(item, index) in projects" :key="item.id" class="border-gray-100 border-b-2 flex flex-col h-32 px-3 py-2">
    <div class="h-1/2 flex items-center w-full">
      <h1 class="w-4/6 font-bold text-md">
        <a href="#" class="cursor-pointer hover:text-gray-500">{{ item.title }}</a>
      </h1>
      <div class="w-1/6 text-right">
        <a href="#" class=""><i class="fas fa-external-link-alt text-gray-500 hover:text-black"></i></a>
      </div>
      <div class="w-1/6 text-right sm:pr-5">
        <button v-if="!item.stared" @click="toggleStar(index)"><i class="far fa-star cursor-pointer text-gray-500 hover:text-black"></i></button>
        <button v-else @click="toggleStar(index)"><i class="fas fa-star cursor-pointer text-yellow-400 hover:text-yellow-300"></i></button>
      </div>
    </div>
    <div class="h-1/2 sm:flex items-center w-full text-gray-500">
      <div class="w-full sm:w-1/2">
        <p><i class="fab fa-github fa-lg mr-2"></i>{{ user.id }}/{{ item.id }}</p>
      </div>
      <div class="w-full sm:w-1/2 pr-5 flex sm:justify-end items-center">
        <p class="mr-3">{{ item.language }}</p>
        <p class="mr-3">・</p>
        <p>Updated {{ item.updated_at }}</p>
      </div>
    </div>
  </article>
</template>

<script>
export default {
  data(){
    return {
      user: {
        id: "tailwind"
      },
      projects: [
        {
          title: "Tailwind Practice",
          stared: true,
          id: "tailwind-practice",
          language: "Vue.js",
          updated_at: "2h ago",
        },
        {
          title: "Vue3 Practice",
          stared: false,
          id: "vue3-practice",
          language: "Vue.js",
          updated_at: "4h ago",
        }
      ]
    }
  },
  methods: {
    toggleStar(index){
      const project = this.projects[index]
      project.stared ? project.stared = false : project.stared = true
    }
  }
}
</script>

<style>

</style>
