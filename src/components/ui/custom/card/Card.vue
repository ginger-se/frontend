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
    <div class="bg-white  w-fit mx-auto flex flex-col md:flex-row md:justify-center items-center md:gap-4 p-4 rounded-md border shadow-lg">
        <div class="flex flex-col text-center md:text-left ">
            <h3 class="text-2xl font-bold " :class="{'ml-4': description}">{{name}}</h3>
            <p class="text-sm max-w-lg ">{{description}}</p>
        </div>
        <slot/>
        <img v-if="image" :src="image" alt="image" class="max-h-75 w-fit items-center">
    </div>
</template>