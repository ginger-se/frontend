<script setup lang="ts">
import Project from '@/components/ui/custom/card/Project.vue';

</script>

<template>
  <h1 class="text-center text-3xl font-bold">Justin's Projects</h1>
  <div class="   grid grid-cols-1 xl:grid-cols-2 m-2 gap-4">
    <Project
    name="Workout Tracker"
    description="Web application that allows users to build workout plans, track thier progress, and view their history."
    language="PHP with Laravel, Inertia and React"
    image="welcome.png"
    link="https://workout.laravel.cloud/"
    >
    </Project>
    <Project
    name="POS System"
    language="Java with JSwing"
    description="Point of Sale system that allows a cashier to input items, calculate the total, recieve payment, update items in the store, and view sales reports."
    image="POSImage.png"
    video="POSVideo.mp4"
    >
    
    </Project>
    <Project
      name="Vue Todo App"
      language="Vue 3 with Express and MariaDB"
      description="To do list web application that allows users to create, update, and delete lists and list items."
      image="TodoImage.png"
      link="http://ec2-3-135-187-109.us-east-2.compute.amazonaws.com/todo-frontend-vue3/#/"
      >
      
    </Project>
    
    <Project
    name="Maze Solver"
    description="Java program that uses a stack to solve a three dimensional maze. The maze is represented as a three dimensional array with walls, portals, and open spaces."
    language="Java with JSwing"
    image="MazeImage.png"
    video="MazeRecording.mp4"
    >
    
    </Project>
    <Project
    name="Word Finder"
    language="Java with JSwing"
    description="Java program that uses a trie to find words in a block of text."
    image="TrieImage.png"
    video="TrieVideo.mp4"
    >

    </Project>
    <Project
      name="Alien Attack"
      language="C++ with SFML"
      description="Alien attack game that allows the player to move a ship, shoot missiles, and get hit by alien missiles."
      image="SFMLImage.png"
      video="SFMLVideo.mp4"
      >
      

    </Project>
    <Project
      name="Stock Information Website"
      language="JavaScript with Tailwind CSS"
      description="Website that uses a stock API to display current information about the given stock."
      image="stocksImage.png"
      video="StocksVideo.mp4"
      >

    </Project>
    
  </div>
</template>


