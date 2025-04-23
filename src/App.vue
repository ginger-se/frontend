<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>
/*html*/
<template>

  <header>
      <div class = "my-2 bg-white w-fit mx-auto flex justify-center items-center gap-4 rounded-md border p-1 shadow-xs">
        <RouterLink to="/">
          <h3 class="px-2 hover:bg-gray-100 rounded-md">Home</h3>
        </RouterLink>
        <!-- <RouterLink to="/about">
          <h3 class="px-2 hover:bg-gray-100 rounded-md">About</h3>
        </RouterLink> -->
        <RouterLink to="/projects">
          <h3 class="px-2 hover:bg-gray-100 rounded-md">Projects</h3>
        </RouterLink>
        <!-- <RouterLink to="/resume">
          <h3 class="px-2 hover:bg-gray-100 rounded-md">Resume</h3>
        </RouterLink> -->

      </div>
  </header>

  <RouterView />  

  <footer class="border-t min-h-20 grid grid-cols-1 md:w-1/2 md:grid-cols-2 mx-auto">
    <div class="items-center flex flex-col m-auto">

      <p>Email: j.walraven@eagles.oc.edu</p>
      <p>Phone: 405-795-6212</p>
    </div>
    <div class="justify-center flex gap-4 m-auto ">
      <a href="https://github.com/ginger-se" target="_blank"><img src="/github-mark.png" alt="github" class="w-5 h-5"></a>
      <a href="www.linkedin.com/in/justin-walraven-7b573a330" target="_blank"><img src="/LI-In-Bug.png" alt="linkedin" class="w-5 h-5"></a>
    </div>

  </footer>
</template>


