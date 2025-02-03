<script setup>
import { CircleCheck } from 'lucide-vue-next';
const list = ['Cert Manager', 'Helm Charts', 'Operators', 'Linkerd']
</script>

<template>
    <div class="flex h-[45vh] px-[100px] text-[#2B1F51]">
        <div class="h-[95%] flex-1 flex items-center justify-center">
            <img src="/assets/images/click-image.png" alt="Hero Image" />
        </div>
        <div class="flex-1 flex items-end gap-[60px] text-end flex-col ">
            <span class="text-4xl ">
                Get started quickly with one-click apps
            </span>
            <p class="text-[22px] font-light  leading-10">Kubernetes Engine supports integration with popular Kubernetes
                tools, allowing you to create clusters that run pre-configured open source software with one click.
            </p>
            <div class="flex flex-wrap gap-4">
                <div class="flex items-center justify-end p-4 gap-2 w-full sm:w-[calc(50%-1rem)]" v-for="item in list"
                    :key="item">
                    <span class="text-[20px]">{{ item }}</span>
                    <CircleCheck class="w-8 h-8 text-blue-700" />
                </div>
            </div>
        </div>
    </div>
</template>