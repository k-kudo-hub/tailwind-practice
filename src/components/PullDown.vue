<template>
  <div class="relative flex justify-center items-center px-2 mx-auto">
    <button @click="toggle" class="text-white">MENU <i class="fas fa-sort-down"></i></button>
    <transition enter-active-class="duration-200 ease-out" enter-from-class="opacity-0 scale-95" enter-to-class="opacity-100 scale-100" leave-active-class="duration-100 ease-in" leave-from-class="opacity-100 scale-100" leave-to-class="opacity-0 scale-95">
      <ul v-if="isOpen" class="absolute top-16 w-64 p-2 border border-gray-200 bg-blue-300 shadow-md rounded-md">
        <li v-for="(item, id) in menu" :key="id" class="w-full y-full">
          <a :href="item.link" class="flex duration-75 focus:bg-blue-400 hover:bg-blue-400 hover:text-white p-2 text-white w-full y-full block rounded-md">
            <div class="w-1/5 text-white flex items-center">
              <i :class="item.icon" class='fas fa-2x text-white'></i>
            </div>
            <div class="w-4/5">
              <h3 class="font-bold text-lg">{{ item.title }}</h3>
              <p class="leading-4">{{ item.explan }}</p>
            </div>
          </a>
        </li>
      </ul>
    </transition>
  </div>
</template>

<script>
const menu = [
  {
    title: "New project",
    explan: "Create new project",
    link: "#",
    icon: "fa-folder-plus"
  },
  {
    title: "Import projects",
    explan: "Import the project from somewhere",
    link: "#",
    icon: "fa-file-import"
  },
  {
    title: "Set organization",
    explan: "Check your organization's settings",
    link: "#",
    icon: "fa-users-cog"
  },
  {
    title: "Add Member",
    explan: "Add new members to the organization",
    link: "#",
    icon: "fa-user-plus"
  },
]
export default {
  data(){
    return {
      isOpen: false,
    }
  },
  setup() {
    return {
      menu,
    }
  },
  methods: {
    toggle(){
      this.isOpen ? this.isOpen = false : this.isOpen = true;
    }
  },
}
</script>

<style>

</style>