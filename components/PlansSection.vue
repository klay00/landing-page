<script setup>
const cardList = [
    '#FBE06B',
    "#C6CDE0",
    "#69A1E3"
]
</script>

<template>
    <div
        class="text-center relative h-[60vh] mt-[100px] text-[14px] flex flex-col    text-[#2B1F51] w-100 gap-4 justify-center">
        <span class="text-4xl font-bold">Choose plans</span>
        <div class="flex justify-center gap-2 items-center ">
            <div v-for="color in  cardList " :key="card"
                class="transform transition duration-100 hover:scale-110 max-w-xs min-w-[330px] mx-auto bg-white rounded-2xl shadow-lg border overflow-hidden">
                <!-- Header Bar -->
                <div class="h-4 w-full" :style="{ backgroundColor: color }"></div>

                <!-- Content -->
                <div class="p-6 text-center">
                    <h2 class="text-2xl font-bold text-[#092346]">P2-HOST</h2>

                    <div class="flex justify-center items-center gap-4">
                        <div class="mt-2 text-gray-500 text-lg">D.I</div>
                        <div class="text-6xl font-extralight text-[#092346] leading-tight">91.30</div>
                    </div>
                    <div class="flex justify-center items-center gap-4">
                        <div class="mt-1 text-gray-400 text-sm line-through">120 D.L</div>
                        <div class="inline-block bg-[#FEE9DF] text-[#F67A3C] text-xs px-3 py-2 rounded mt-1">
                            30% discount
                        </div>
                    </div>

                    <button
                        class="relative px-8 mt-3 py-2 rounded-[12px] bg-[#092346] text-white isolation-auto z-10 border-2 border-[#092346] transition-all duration-300 hover:bg-transparent hover:text-[#092346] overflow-hidden inline-flex items-center justify-center font-semibold">
                        Order now!
                    </button>

                    <hr class="my-4 border-gray-200">

                    <!-- Features List -->
                    <ul class="text-sm text-gray-700 space-y-4   text-left">
                        <li><strong>60GB</strong> NVMe Storage</li>
                        <li><strong>15</strong> Website(s)</li>
                        <li><strong>4</strong> RAM</li>
                        <li><strong>3</strong> CPU</li>
                        <li>cPanel Control Panel</li>
                        <li><strong class="font-semibold">Unlimited</strong> Subdomains</li>
                        <li><strong class="font-semibold">Unlimited</strong> MySQL & SQL Databases</li>
                        <li><strong class="font-semibold">Unlimited</strong> Email Account</li>
                        <li><strong class="font-semibold">Unlimited</strong> FTP Accounts</li>
                        <li>Dedicated Name Server (ns1, ns2)</li>
                    </ul>
                    <hr class="my-4 border-gray-200">
                    <div class="mt-4 text-center">
                        <a href="#" class="text-gray-700 text-sm font-medium">compare packages</a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>