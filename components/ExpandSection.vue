<script setup>
import { ref } from 'vue';
import { Info, BookOpen, Plus, Minus } from 'lucide-vue-next';

const faqs = ref([
    {
        question: 'What is a Virtual Dedicated Server (VPS)?',
        answer:
            'A virtual server is a server that is divided into completely separate hosting environments. When you have VPS hosting, one of those environments is entirely dedicated to you. This means you don\'t have to share resources (such as RAM or CPU) with other clients and are less likely to be affected by their behavior.',
        isOpen: true,
    },
    {
        question: 'When should I use VPS hosting instead of shared hosting?',
        answer: 'VPS hosting is best used when you need more control over your hosting environment, require dedicated resources, or want better performance and security compared to shared hosting.',
        isOpen: false,
    },
    {
        question: 'What is the difference between a virtual server and a dedicated server?',
        answer: 'A virtual server is a part of a larger server divided into separate environments, whereas a dedicated server is an entire physical server dedicated to one user.',
        isOpen: false,
    },
    {
        question: 'What sites are available for VPS hosting?',
        answer: 'Many hosting providers offer VPS hosting, including AWS, DigitalOcean, Linode, and Vultr.',
        isOpen: false,
    },
]);

const toggleFAQ = (index) => {
    faqs.value[index].isOpen = !faqs.value[index].isOpen;
};
</script>

<template>
    <div class="flex space-x-6 p-6 mx-[100px] ">
        <div class="w-1/4 space-y-4">
            <div class="flex items-center min-h-[250px] justify-center flex-col gap-5 p-4 bg-white rounded-lg">
                <img src="/assets/images/faq-icon.png" alt="Hero Image" />
                <span class="ml-4 text-2xl font-medium">Frequently asked questions</span>
            </div>
            <div class="flex items-center min-h-[250px]  justify-center flex-col gap-5 p-4 bg-white rounded-lg">
                <img src="/assets/images/call-center.png" alt="Hero Image" />
                <span class="ml-4 text-2xl font-medium">Help Center</span>
            </div>
        </div>

        <div class="w-3/4 bg-white p-6 rounded-lg ">
            <div v-for="(faq, index) in faqs" :key="index" class="py-[40px]">
                <button @click="toggleFAQ(index)"
                    class="flex justify-between items-center w-full text-left text-lg font-semibold text-gray-800">
                    <span>{{ faq.question }}</span>
                    <component :is="faq.isOpen ? Minus : Plus" class="w-6 h-6 text-gray-600" />
                </button>
                <p v-if="faq.isOpen" class="mt-2 text-gray-600 text-[16px] leading-8">{{ faq.answer }}</p>
            </div>
        </div>
    </div>
</template>
