<script setup lang="ts">
import { Drill, BadgeCheck, Shield, CircleDollarSign, Mail, Phone, Fence, Sprout, Snowflake } from 'lucide-vue-next';

const imageArr1 = [
    '/1.png',
    '/2.png',
    '/3.png',
    '/4.png',
    '/5.png',
    '/6.png',
    '/7.png',
    '/8.png',
    '/9.png',
    '/10.png',
    '/11.png',
    '/12.png',
    '/13.png',
];

const imageArr2 = [
    '/14.png',
    '/15.png',
    '/16.png',
    '/17.png',
    '/18.png',
    '/19.png',
    '/20.png',
    '/21.png',
    '/22.png',
    '/23.png',
    '/24.png',
    '/25.png',
    '/26.png',
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
                <UCarousel v-slot="{ item }" loop :auto-scroll="{ direction: 'backward', speed: 1 }" :items="imageArr1"
                    :ui="{ item: 'basis-1/4' }">
                    <NuxtImg :src="item" width="600" height="500" fit="cover" class="rounded-xl shadow " />
                </UCarousel>
                <UCarousel v-slot="{ item }" loop :auto-scroll="{ speed: 1 }" :items="imageArr2"
                    :ui="{ item: 'basis-1/4' }">
                    <NuxtImg :src="item" width="600" height="500" fit="cover" class="rounded-xl shadow" />
                </UCarousel>
            </div>
        </section>
        <section class=" bg-[#F5EFE1] py-10">
            <h2 class=" text-center text-2xl md:text-4xl font-title text-slate-700">What our Clients Say</h2>
            <p class=" text-center px-5 md:w-2/3 md:mx-auto font-body mt-5 text-gray-600">Building trust, one project at
                a time.</p>
            <div class=" grid grid-cols-1 md:grid-cols-3 gap-5 md:gap-10 px-10 md:w-4/5 md:mx-auto mt-10">
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">" You built our new deck last summer, the team was
                        professional, fast, and paid attention to every detail.
                        We’ve been enjoying our backyard more than ever!"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar
                            src="https://images.unsplash.com/photo-1564564321837-a57b7070ac4f?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8N3x8bWFufGVufDB8fDB8fHww" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Sarah M</p>
                            <p class=" font-title text-xs text-slate-400">Waterloo,ON</p>
                        </div>
                    </div>
                </div>
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">"We hired Hu for fence installation and ongoing
                        lawn care. Their work is clean, reliable, and always on time. The crew truly cares about
                        customer satisfaction!"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar
                            src="https://images.unsplash.com/photo-1563306406-e66174fa3787?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NTB8fHdvbWFufGVufDB8fDB8fHww" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Daniel K</p>
                            <p class=" font-title text-xs text-slate-400">Cambridge, ON</p>
                        </div>
                    </div>
                </div>
                <div class=" flex flex-col justify-between p-5 bg-white h-52 rounded-xl shadow-md">
                    <p class=" font-body text-slate-500 ">
                        "去年冬天雪特别大，多亏了胡的除雪服务，车道都清理得干干净净，非常省心。他们真的很可靠，今年我会继续使用他们的服务。"</p>
                    <div class=" self-end flex items-center gap-2">
                        <UAvatar
                            src="https://plus.unsplash.com/premium_photo-1682093665127-6610b9ccb0dc?w=500&auto=format&fit=crop&q=60&ixlib=rb-4.1.0&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NDl8fHdvbWFuJTIwYXNpYXxlbnwwfHwwfHx8MA%3D%3D" />
                        <div>
                            <p class=" font-title text-sm text-slate-700">Liu</p>
                            <p class=" font-title text-xs text-slate-400">Kitchener, ON</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <section
            class=" md:w-5/7 md:mx-auto flex flex-col md:flex-row items-center md:items-start justify-center gap-10">
            <img src="/carpentry.png" alt="a man is doing carpentry work" class=" w-72 rounded-2xl ">
            <div class=" px-5 md:px-0 md:py-5">
                <h2 class="text-2xl md:text-4xl font-title text-slate-700">Trusted Local Landscape Partners
                </h2>
                <p class=" font-body mt-5 text-gray-600">Hu Landscaping is a proud Waterloo-area team building and
                    maintaining outdoor spaces that reflect the way you live. From tailored deck and fence work to
                    seasonal lawn and snow services, we blend thoughtful design, long-term durability, and
                    straight-forward communication so every project is completed with care, transparency, and a focus on
                    lasting value.</p>
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
