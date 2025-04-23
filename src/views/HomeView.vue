<script setup>
import Card from '@/components/ui/custom/card/Card.vue';

</script>

<template>
  <main class="h-full flex flex-col justify-center gap-10 items-center">
    <Card 
    name="Justin Walraven"
    description="Computer Science Student at Oklahoma Christian University. Enjoys writing code and solving complex problems. Currently
     works as a programming tutor at OC where he helps students understand concepts, finish projects, and debug their code. 
     other intrests include bouldering, studying theology, working out, and watching football." 
    image="headshot.jpg"
    />
    <a target="_blank" href="WalravenResume.pdf" >
    <Card
      name="Resume"
      
    >
    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-file-icon lucide-file"><path d="M15 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7Z"/><path d="M14 2v4a2 2 0 0 0 2 2h4"/></svg>
    </Card>
    </a>
  </main>
</template>
