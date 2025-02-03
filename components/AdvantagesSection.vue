<script setup>
// Define an array of image paths
import Icon1 from '@/assets/images/1.png';
import Icon2 from '@/assets/images/2.png';
import Icon3 from '@/assets/images/3.png';
import Icon4 from '@/assets/images/4.png';
import Icon5 from '@/assets/images/5.png';
import Icon6 from '@/assets/images/6.png';
import Icon7 from '@/assets/images/7.png';
import Icon8 from '@/assets/images/8.png';


// Define an array of image paths
const images = [
    { title: 'Easy to use tool', id: 1, src: Icon1 },
    { title: 'Responsive design on various devices', id: 1, src: Icon2 },
    { title: 'Support 50 languages', id: 1, src: Icon3 },
    { title: 'Multilingual websites', id: 1, src: Icon4 },
    { title: 'The ability to transfer sites from  other building tools', id: 1, src: Icon5 },
    { title: 'More than a million templates', id: 1, src: Icon6 },
    { title: 'Plugins', id: 1, src: Icon7 },
    { title: 'Video lessons on how to use', id: 1, src: Icon8 },
];
</script>

<template>
    <div class="text-center relative h-[80vh]  flex items-end  mb-4  text-[#2B1F51] w-100 gap-4 justify-center">
        <!-- Background images -->
        <div class="h-[95%] absolute z-[-1] right-0 top-[200px]">
            <img src="/assets/images/right-blocks-graphic.png" alt="Hero Image" />
        </div>
        <div class="h-[95%] absolute z-[-1] left-0 top-[200px]">
            <img src="/assets/images/right-blocks-graphic.png" alt="Hero Image" class="transform scale-x-[-1]" />
        </div>

        <!-- Content -->
        <div class="flex flex-col items-center gap-9 ">
            <span class="text-4xl font-bold">
                Advantages
            </span>
            <span class="text-xl font-light">
                Basic benefits in all our plans
            </span>
            <div class="flex items-center justify-center">
                <div class="grid grid-cols-4 gap-8">
                    <!-- Loop through the images array -->
                    <div v-for="image in images" :key="image.id"
                        class="transform transition duration-100 min-w-[255px] flex flex-col items-center text-center gap-3 p-5 hover:scale-110 rounded-lg shadow-[0_0_20px_0_rgba(0,0,0,0.1)] h-[210px] max-w-[296px] hover:shadow-[0_0_25px_0_rgba(0,0,0,0.15)] bg-white">
                        <img :src="image.src" :alt="`Icon ${image.id}`" />
                        <h2 class="font-semibold px-4">{{ image.title }}</h2>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>