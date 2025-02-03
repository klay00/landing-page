<template>
    <section class=" flex flex-col justify-end items-center py-16 px-[10%] ">
        <div class="relative w-[100%] h-[240px] bg-[#333C5E] flex flex-col justify-center items-center gap-5">
            <div class="absolute bottom-0 left-[50px]">
                <img src="/assets/svg/one-block.svg" alt="Hero Image" />
            </div>
            <div class="absolute bottom-0 right-[50px]">
                <img src="/assets/svg/blockes.svg" alt="Hero Image" />
            </div>
            <div class="flex flex-col items-center gap-5">
                <h3 class="text-4xl font-bold text-white">Do you need licenses to run your server?</h3>
                <h3 class="text-4xl font-bold text-white">We provide it to you at the lowest cost</h3>
                <button
                    class="relative px-8 py-2 rounded-[12px] bg-white isolation-auto z-10 border-2 border-[#092346] before:absolute before:w-full before:transition-all before:duration-700 before:hover:w-full hover:text-white before:-right-full before:hover:right-0 before:rounded-full before:bg-[#092346] before:-z-10 before:aspect-square before:hover:scale-150 overflow-hidden before:hover:duration-700 inline-flex items-center justify-center px-4 py-3 text-sm font-semibold text-black bg-white border border-[#092346] rounded-lg shadow-sm gap-x-2 hover:bg-gray-50  disabled:pointer-events-none">
                    Order now!
                </button>
            </div>
        </div>
    </section>
</template>