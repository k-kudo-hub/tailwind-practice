<template>
  <div class="relative w-1/3 flex justify-center items-center px-2">
    <button @click="toggleBlog" class="text-white">blog <i class="fas fa-sort-down"></i></button>
    <transition enter-active-class="duration-200 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
      <ul v-if="isBlogOpen" class="absolute top-16 w-64 p-2 border border-gray-200 bg-blue-300 shadow-md rounded-md">
        <li v-for="(item, id) in blog" :key="id" class="w-full y-full">
          <a :href="item.link" class="flex duration-75 focus:bg-blue-400 hover:bg-blue-400 hover:text-white p-2 text-white w-full y-full block rounded-md">
            <div class="w-1/5 text-white flex items-center">
              <i :class="item.icon" class='fas fa-2x text-white'></i>
            </div>
            <div class="w-4/5">
              <h3 class="font-bold text-lg">{{ item.title }}</h3>
              <p>{{ item.explan }}</p>
            </div>
          </a>
        </li>
      </ul>
    </transition>
  </div>
  <div class="relative w-1/3 flex justify-center items-center px-2">
    <button @click="toggleComponents" class="text-white">components <i class="fas fa-sort-down"></i></button>
    <transition enter-active-class="duration-200 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
      <ul v-if="isComponentsOpen" class="absolute top-16 w-64 p-2 border border-gray-200 bg-blue-300 shadow-md rounded-md">
        <li v-for="(item, id) in components" :key="id" class="w-full y-full">
          <a :href="item.link" class="flex duration-75 focus:bg-blue-400 hover:bg-blue-400 hover:text-white p-2 text-white w-full y-full block roundeΩd-md">
            <div class="w-1/5 text-white flex items-center">
              <i :class="item.icon" class='fas fa-2x text-white'></i>
            </div>
            <div class="w-4/5">
              <h3 class="font-bold text-lg">{{ item.title }}</h3>
              <p>{{ item.explan }}</p>
            </div>
          </a>
        </li>
      </ul>
    </transition>
  </div>
  <div class="w-1/3 flex justify-center items-center px-2">
    <a href="#" class="text-gray-100 hover:text-white text-lg">cheats sheet</a>
  </div>
</template>

<script>
const blog = [
  {
    title: "Team blog",
    explan: "enjoy our blog!",
    link: "#",
    icon: "fa-blog"
  },
  {
    title: "Developper blog", 
    explan: "enjoy our blog!", 
    link: "#",
    icon: "fa-file-code"
  },
]
const components = [
  {
    title: "Components",
    explan: "Check all components",
    link: "#",
    icon: "fa-gem"
  }
]
export default {
  data(){
    return {
      isBlogOpen: false,
      isComponentsOpen: false,
    }
  },
  setup() {
    return {
      blog,
      components,
    }
  },
  methods: {
    toggleBlog(){
      if(this.isBlogOpen){
        this.isBlogOpen = false;
      } else {
        this.isBlogOpen = true;
        this.isComponentsOpen = false;
      }
    },
    toggleComponents(){
      if(this.isComponentsOpen){
        this.isComponentsOpen = false;
      } else {
        this.isComponentsOpen = true;
        this.isBlogOpen = false;
      }
    },
    closeModals(){
      this.isBlogOpen = false;
      this.isComponentsOpen = false;
    }
  },
}
</script>

<style>

</style>