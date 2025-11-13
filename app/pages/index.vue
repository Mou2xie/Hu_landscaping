<script setup lang="ts">
import { Drill } from 'lucide-vue-next';

const items = [
    'https://picsum.photos/468/468?random=1',
    'https://picsum.photos/468/468?random=2',
    'https://picsum.photos/468/468?random=3',
    'https://picsum.photos/468/468?random=4',
    'https://picsum.photos/468/468?random=5',
    'https://picsum.photos/468/468?random=6'
]
</script>

<template>
    <div class=" space-y-20">
        <section
            class=" bg-[url(/hero-image.png)] bg-center bg-cover bg-no-repeat h-80 md:h-140 relative flex flex-col justify-center items-center">
            <div class=" bg-black opacity-30 absolute inset-0"></div>
            <div class=" text-white text-center text-3xl md:text-7xl z-10 font-title">
                Crafting Beautiful Outdoor Spaces
            </div>
            <div class=" font-body text-stone-100 z-10 md:text-xl italic md:mt-3 ">
                Decks | Fence | Lawn | Snow Removal
            </div>
        </section>
        <section>
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">Our Services</h2>
            <p class=" px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">At Waterloo Carpentry & Outdoors, we
                specialize in transforming your outdoor areas into beautiful, functional spaces. From custom-built decks
                and fences to meticulous lawn care and reliable snow removal, our team brings expertise and a commitment
                to quality to every project. We are dedicated to delivering durable, high-quality results that you can
                enjoy for years to come.</p>
            <div class=" grid grid-cols-1 md:grid-cols-4 gap-5 md:gap-10 px-10 md:w-4/5 md:mx-auto mt-10">
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-40 rounded-xl shadow-md">
                    <Drill color="#6A8B64" :size="32" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Deck Building</p>
                    <p class=" text-center font-body text-gray-500">Custom designs for stunning, durable decks.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-40 rounded-xl shadow-md">
                    <Drill color="#6A8B64" :size="32" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Deck Building</p>
                    <p class=" text-center font-body text-gray-500">Custom designs for stunning, durable decks.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5  bg-white h-40 rounded-xl shadow-md">
                    <Drill color="#6A8B64" :size="32" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Deck Building</p>
                    <p class=" text-center font-body text-gray-500">Custom designs for stunning, durable decks.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-40 rounded-xl shadow-md">
                    <Drill color="#6A8B64" :size="32" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Deck Building</p>
                    <p class=" text-center font-body text-gray-500">Custom designs for stunning, durable decks.</p>
                </div>
            </div>
        </section>
        <section>
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">Our Work</h2>
            <p class=" text-center px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">A showcase of our dedication
                to quality.</p>
            <div class=" mt-10">
                <UCarousel v-slot="{ item }" loop auto-scroll :items="items" :ui="{ item: 'basis-1/4' }">
                    <img :src="item" width="500" height="300" class="rounded-xl">
                </UCarousel>
            </div>
        </section>
        <section class=" bg-[#F5EFE1]">
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">What our Clients Say</h2>
            <p class=" text-center px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">Building trust, one project at a time.</p>
            <div class=" mt-10">
                
            </div>
        </section>
    </div>
</template>