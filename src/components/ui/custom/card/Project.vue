<script setup>
import { ref } from 'vue';
import Button from '../../button/Button.vue';
import { onClickOutside } from '@vueuse/core';
import { CirclePlay } from 'lucide-vue-next';
const props = defineProps({
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
    link: {
        type: String,
        required: false,
    },
    video: {
        type: String,
        required: false,
    },
    language: {
        type: String,
        required: true,
    },

})



let play=ref(false);
let videoRef=ref(null);
 function   playVideo() {
        play.value=true;
        if(props.video){
                if (videoRef) {
                    videoRef.value.play();
                }

        }

    }
  function  closeVideo() {
        play.value=false;
        if (videoRef) {
            videoRef.value.pause();
        }
    }

const target = videoRef;

onClickOutside(target, closeVideo);

</script>

<template>
    <div class="bg-white  w-full  mx-auto md:grid md:grid-cols-2 md:items-center md:gap-4 p-4 rounded-md border shadow-lg">
        <div class="grid grid-cols-1 gap-2 text-center md:text-left ">
            <h3 class="text-2xl font-bold " >{{name}}</h3>
            <h5 class="text-md font-bold ">Stack: {{language}}</h5>
            <p class="text-sm ">{{description}}</p>
            <a :href="link" target="_blank" v-if="link"><Button  variant="outline">Click to try project</Button></a>
        </div>
        <div class="max-h-full min-h-50 relative" @click="playVideo()" >
            <img v-if="image" :src="image" alt="image"   class="border  shadow-md">
            <CirclePlay v-if="props.video" class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 cursor-pointer text-red-500"
                color:black
            />
            
        </div>
        <div v-if="props.video" v-show="play"  class=" fixed left-0 top-0 z-10 bg-gray-700/50 h-screen w-screen flex justify-center items-center">
            <video  ref="videoRef" :src="video" muted controls class="m-auto w-2/3" >
                Your browser does not support the video tag.
            </video>
            <h1>Click background to exit</h1>
        </div>
    </div>
</template>