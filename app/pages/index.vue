<script setup lang="ts">
import { Drill, BadgeCheck, Shield, CircleDollarSign, Mail, Phone, Fence, Sprout, Snowflake } from 'lucide-vue-next';

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
            <div class=" text-white text-center text-3xl md:text-6xl z-10 font-title">
                Crafting Beautiful Outdoor Spaces
            </div>
            <div class=" font-body text-stone-200 z-10 font-semibold md:text-xl italic md:mt-3 ">
                Decks | Fence | Lawn | Snow Removal
            </div>
        </section>
        <section>
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">Our Services</h2>
            <p class=" px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">Hu Landscaping Inc. provides reliable deck
                building, fence installation, lawn care, and snow removal services across Waterloo, Kitchener,
                Cambridge, and surrounding areas. We combine quality craftsmanship with dependable year-round property
                care to keep your outdoor space looking its best in every season.</p>
            <div class=" grid grid-cols-1 md:grid-cols-4 gap-5 md:gap-10 px-10 md:w-4/5 md:mx-auto mt-10">
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-48 rounded-xl shadow-md">
                    <Drill color="#6A8B64" :size="40" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Deck Building</p>
                    <p class=" text-center font-body text-sm text-gray-500 mt-1">Custom designs for stunning, durable
                        decks.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-48 rounded-xl shadow-md">
                    <Fence color="#6A8B64" :size="40" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Fence Installation</p>
                    <p class=" text-center font-body text-sm text-gray-500 mt-1">Secure and stylish fences for your
                        property.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-48 rounded-xl shadow-md">
                    <Sprout color="#6A8B64" :size="40" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Lawn Care</p>
                    <p class=" text-center font-body text-sm text-gray-500 mt-1">Expert care to keep your lawn healthy
                        and vibrant.</p>
                </div>
                <div class=" flex flex-col justify-center items-center p-5 bg-white h-48 rounded-xl shadow-md">
                    <Snowflake color="#6A8B64" :size="40" />
                    <p class=" font-title text-slate-700 text-xl mt-3">Snow Removal</p>
                    <p class=" text-center font-body text-sm text-gray-500 mt-1">Reliable snow clearing for safe access.
                    </p>
                </div>
            </div>
        </section>
        <section>
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">Our Work</h2>
            <p class=" text-center px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">A showcase of our dedication
                to quality.</p>
            <div class=" mt-10 space-y-10">
                <UCarousel v-slot="{ item }" loop :auto-scroll="{ direction: 'backward', speed: 1 }" :items="items"
                    :ui="{ item: 'basis-1/4' }">
                    <img :src="item" width="500" height="300" class="rounded-xl">
                </UCarousel>
                <UCarousel v-slot="{ item }" loop :auto-scroll="{ speed: 1 }" :items="items"
                    :ui="{ item: 'basis-1/4' }">
                    <img :src="item" width="500" height="300" class="rounded-xl">
                </UCarousel>
            </div>
        </section>
        <section class=" bg-[#F5EFE1] py-10">
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">What our Clients Say</h2>
            <p class=" text-center px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">Building trust, one project at
                a time.</p>
            <div class=" grid grid-cols-1 md:grid-cols-3 gap-5 md:gap-10 px-10 md:w-4/5 md:mx-auto mt-10">
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">"The new deck is absolutely fantastic! The
                        craftsmanship is top-notch and the team was professional from start to finish. Highly
                        recommended!"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar src="https://github.com/benjamincanac.png" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Benjamin Canac</p>
                            <p class=" font-title text-xs text-slate-400">Waterloo,ON</p>
                        </div>
                    </div>
                </div>
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">"The new deck is absolutely fantastic! The
                        craftsmanship is top-notch and the team was professional from start to finish. Highly
                        recommended!"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar src="https://github.com/benjamincanac.png" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Benjamin Canac</p>
                            <p class=" font-title text-xs text-slate-400">Waterloo,ON</p>
                        </div>
                    </div>
                </div>
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">"The new deck is absolutely fantastic! The
                        craftsmanship is top-notch and the team was professional from start to finish. Highly
                        recommended!"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar src="https://github.com/benjamincanac.png" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Benjamin Canac</p>
                            <p class=" font-title text-xs text-slate-400">Waterloo,ON</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section
            class=" md:w-5/7 md:mx-auto flex flex-col md:flex-row items-center md:items-start justify-center gap-10">
            <img src="/carpentry.png" alt="a man is doing carpentry work" class=" w-72 rounded-2xl ">
            <div class=" px-5 md:px-0 md:py-5">
                <h2 class="text-2xl md:text-4xl font-title text-slate-700">Your Local Outdoor expertise
                </h2>
                <p class=" font-body mt-5 text-gray-600">Waterloo Carpentry &
                    Outdoors is a locally-owned business dedicated to enhancing the beauty and functionality of your
                    outdoor living spaces. We combine years of experience with a passion for quality work, ensuring
                    every project meets our high standards and your complete satisfaction. Honesty, integrity, and
                    community are at the heart of everything we do.</p>
                <div class=" px-5 md:w-4/5 md:mx-auto grid grid-cols-3 gap-10 mt-10">
                    <div class=" flex flex-col items-center gap-2">
                        <BadgeCheck color="#6A8B64" :size="40"></BadgeCheck>
                        <p class=" text-slate-600 font-title text-center">Fully Licensed</p>
                    </div>
                    <div class=" flex flex-col items-center gap-2">
                        <Shield color="#6A8B64" :size="40"></Shield>
                        <p class=" text-slate-600 font-title text-center">Insured & Bonded</p>
                    </div>
                    <div class=" flex flex-col items-center gap-2">
                        <CircleDollarSign color="#6A8B64" :size="40"></CircleDollarSign>
                        <p class=" text-slate-600 font-title text-center">Free estimates</p>
                    </div>
                </div>
            </div>
        </section>
        <section id="contact" class=" bg-[#F5EFE1] py-10">
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">Contact Us</h2>
            <p class=" text-center px-5 md:w-1/2 md:mx-auto font-body mt-5 text-gray-600">Reach out by phone or email
                for a free, no-obligation estimate. We're here to answer your questions and help bring your vision to
                life.</p>
            <div class=" flex justify-center mt-10">
                <div class=" space-y-5">
                    <div class=" flex items-center gap-5">
                        <div class=" w-10 h-10 rounded-3xl flex justify-center items-center bg-slate-600">
                            <Phone color="white" :size="22" />
                        </div>
                        <p class=" text-xl font-title font-semibold text-slate-600">437 - 259 - 0245</p>
                    </div>
                    <div class=" flex items-center gap-5">
                        <div class=" w-10 h-10 rounded-3xl flex justify-center items-center bg-slate-600">
                            <Mail color="white" :size="22" />
                        </div>
                        <p class=" text-xl font-title font-semibold text-slate-600">kongqihu91@gmail.com</p>

                    </div>
                </div>
            </div>
        </section>
    </div>
</template>