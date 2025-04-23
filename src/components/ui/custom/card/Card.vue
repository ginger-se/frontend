<script setup>
defineProps({
  name: {
    type: String,
    required: true,
  },
    description: {
        type: String,
        required: true,
    },
    image: {
        type: String,
        required: true,
    },
})
</script>

<template>
    <div class="bg-white  w-fit mx-auto md:flex md:justify-center md:items-center md:gap-4 p-4 rounded-md border shadow-lg">
        <div class="flex flex-col items-left ">
            <h3 class="text-2xl font-bold " :class="{'ml-4': description}">{{name}}</h3>
            <p class="text-sm max-w-lg ">{{description}}</p>
        </div>
        <slot/>
        <img v-if="image" :src="image" alt="image" class="max-h-75">
    </div>
</template>