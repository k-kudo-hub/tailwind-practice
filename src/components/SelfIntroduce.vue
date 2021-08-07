<template>
  <div class="h-24 w-full p-4 flex mb-2">
    <div class="w-1/3 flex justify-center items-center">
      <img src="../assets/logo.png" alt="" class="h-12 w-12 rounded-3xl">
    </div>
    <div class="w-2/3 py-2">
      <h2 class="font-bold">Geoge Williams</h2>
      <p class="text-gray-500 hover:text-gray-700 focus:text-gray-700 text-sm"><a href="#">@tailwind_0123</a></p>
    </div>
  </div>
  <div class="h-32 w-full p-4 flex flex-col mb-2">
    <a href="#" class="w-11/12 mx-auto border border-blue-300 mb-3 p-2 rounded-3xl bg-blue-300 text-white text-center shadow-md hover:bg-blue-400 focus:bg-blue-400">New Project</a>
    <a href="#" class="w-11/12 mx-auto border p-2 rounded-3xl shadow-md hover:bg-gray-200 focus:bg-gray-200 text-center">Invite Team</a>
  </div>
  <div class="h-32 container p-4 flex">
    <div class="mx-auto flex flex-col">
      <div class="h-1/2 flex">
        <i class="fas fa-user-friends mr-2 text-gray-500 w-1/12"></i>
        <p class="leading-3">
          <a href="#" class="mr-1 text-gray-500 hover:text-black text-sm">124 followers</a>/
          <a href="#" class="text-gray-500 hover:text-black text-sm">122 following</a>
        </p>
      </div>
      <div class="h-1/4 flex">
        <i class="fas fa-briefcase mr-2 text-gray-500 w-1/12"></i>
        <a href="#" class="mr-1 text-gray-500 hover:text-black text-sm">12 projects</a>
      </div>
    </div>
    </div>
</template>

<script>
export default {
  data(){
    return {

    }
  }
}
</script>

<style>

</style>
