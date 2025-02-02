<script setup>
// Define an array of image paths
import Icon1 from '@/assets/svg/icon-1.svg';
import Icon2 from '@/assets/svg/icon-2.svg';
import Icon3 from '@/assets/svg/icon-3.svg';

// Define an array of image paths
const images = [
    { id: 1, src: Icon1, title: "Block unauthorized email", description: "Quickly configure, manage and publish your groups in simple steps and with zero downtime." },
    { id: 2, src: Icon2, title: "Feature 2", description: "Quickly configure, manage and publish your groups in simple steps and with zero downtime." },
    { id: 3, src: Icon3, title: "Feature 3", description: "Quickly configure, manage and publish your groups in simple steps and with zero downtime." },
];
</script>

<template>
    <div class="text-center relative h-[60vh]  flex items-end  mb-4  text-[#2B1F51] w-100 gap-4 justify-center">
        <!-- Background images -->
        <div class="h-[95%] absolute z-[-1] right-0">
            <img src="/assets/images/right-blocks-graphic.png" alt="Hero Image" />
        </div>
        <div class="h-[95%] absolute z-[-1] left-0">
            <img src="/assets/images/right-blocks-graphic.png" alt="Hero Image" class="transform scale-x-[-1]" />
        </div>

        <!-- Content -->
        <div class="flex flex-col items-center gap-9 ">
            <span class="text-4xl font-bold">
                Go faster and grow your business
            </span>
            <div class="flex   items-center gap-4">
                <!-- Loop through the images array -->
                <div v-for="image in images" :key="image.id"
                    class="transform transition duration-100 flex flex-col items-end text-end gap-3 p-5 hover:scale-110 rounded-lg shadow-[0_0_20px_0_rgba(0,0,0,0.1)] h-[270px] max-w-[370px] hover:shadow-[0_0_25px_0_rgba(0,0,0,0.15)] bg-white">
                    <img :src="image.src" :alt="`Icon ${image.id}`" />
                    <h2 class="font-semibold px-4">{{ image.title }}</h2>
                    <p class="font-light leading-8  px-4">{{ image.description }}</p>
                </div>
            </div>
        </div>
    </div>
</template>