<script setup>
const list = [
    { id: '3', desc: 'Get many of the plugins, tools, and functionality you need to optimize your site. Including the basics like your photo gallery, media, social media platforms, and more.', title: 'Enhance your sites functionality' },
    { id: '4', desc: 'Take a look at your website with the selected template, before you publish it publicly.', title: 'Preview the site' },
    { id: '5', desc: 'You can publish your site on the Internet, or save a draft of your site without publishing it.', title: 'Publish or save your site – with one click' }
]
</script>

<template>
    <section class="py-16 bg-gray-50 text-center h-[80vh]">
        <h2 class="text-3xl font-bold mb-12 text-gray-900">Build your website easily with our website builder</h2>
        <div class="flex flex-grow  gap-4 mt-4" style="height: 100%;">
            <div class="flex items-center justify-evenly flex-col flex-1">
                <div class="">
                    <img src="/assets/images/wheb-left.png" alt="Hero Image" />
                </div>
                <div>
                    <div>
                        <div class="flex flex-col items-end text-end space-y-4">
                            <div
                                class="relative w-16 h-16 flex items-center justify-center rounded-full border-4 border-blue-500">
                                <div
                                    class="w-12 h-12 flex items-center justify-center rounded-full bg-blue-500 text-white text-lg font-bold">
                                    1
                                </div>
                            </div>
                            <div class="text-start">
                                <h2 class="text-xl mb-4 font-semibold text-gray-900 text-start">Choose your own template
                                </h2>
                                <p class="text-gray-700">Choose from 200 amazing templates to start building your
                                    website.
                                </p>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="flex items-center flex-col">
                <div class="flex-1"></div>
                <div class="w-5 h-5 bg-[#1B69FF] rounded-full"></div>
                <div style="min-height: 350px;" class="flex-1  border border-[#1B69FF]"></div>
                <div class="w-5 h-5 bg-[#1B69FF] rounded-full"></div>
                <div class="flex-1"></div>
            </div>
            <div class="flex items-center justify-evenly flex-col flex-1">

                <div>
                    <div>
                        <div class="flex flex-col  space-y-4">
                            <div
                                class="relative w-16 h-16 flex items-center justify-center rounded-full border-4 border-blue-500">
                                <div
                                    class="w-12 h-12 flex items-center justify-center rounded-full bg-blue-500 text-white text-lg font-bold">
                                    1
                                </div>
                            </div>
                            <h2 class="text-xl text-end font-semibold text-gray-900">Choose your own template</h2>
                            <p class="text-gray-700">Choose from 200 amazing templates to start building your website.
                            </p>
                        </div>
                    </div>
                </div>
                <div class="">
                    <img src="/assets/images/web-right.png" alt="Hero Image" />
                </div>
            </div>
        </div>
        <div class="flex flex-col items-center mt-14 gap-9 w-100">
            <div class="flex items-center gap-8">
                <!-- Loop through the images array -->
                <div v-for="item in list" :key="item.id"
                    class="transform transition duration-100 flex flex-col items-end text-end gap-3 p-5 hover:scale-110 rounded-lg shadow-[0_0_20px_0_rgba(0,0,0,0.1)] h-[270px] max-w-[370px] hover:shadow-[0_0_25px_0_rgba(0,0,0,0.15)] bg-white">
                    <div
                        class="relative w-16 h-16 flex items-center justify-center rounded-full border-4 border-blue-500">
                        <div
                            class="w-12 h-12 flex items-center justify-center rounded-full bg-blue-500 text-white text-lg font-bold">
                            {{ item.id }}
                        </div>
                    </div>
                    <h2 class="font-semibold px-4">{{ item.title }}</h2>
                    <p class="font-light leading-8  px-4">{{ item.desc }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped></style>
