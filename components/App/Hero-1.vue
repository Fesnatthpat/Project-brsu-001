<script setup lang="ts">
import { ref } from "vue";

useHead({
    title: 'หน้าหลัก'
})

const slides = [
    { img: "images/1.jpg", text: "Welcome" },
    { img: "images/2.jpg", text: "Discover" },
    { img: "images/3.jpg", text: "Explore" },
];

const current = ref(0);
const changeSlide = (i: number) => current.value = (i + slides.length) % slides.length;
</script>

<template>
    <div
        class="min-h-[300px] md:min-h-[600px] bg-gradient-to-t from-[#a9c9fb] to-[#1c66d6] flex items-center justify-center p-4">
        <div class="relative w-full max-w-[1100px] aspect-[16/9] md:aspect-[1100/350] rounded-lg overflow-hidden">
            <!-- Slide -->
            <div class="w-full h-[250px] md:h-full relative">
                <img :src="slides[ current ].img" alt="slide" class="w-full h-full object-cover">
                <h2
                    class="absolute inset-0 flex items-center justify-center text-2xl md:text-4xl font-bold text-white bg-black/40">
                    {{ slides[ current ].text }}
                </h2>
            </div>

            <!-- Navigation -->
            <button @click="changeSlide(current - 1)"
                class="absolute left-2 top-1/2 -translate-y-1/2 bg-white/80 hover:bg-white p-2 rounded-full">
                <svg class="w-5 h-5 md:w-6 md:h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="m15 19-7-7 7-7" />
                </svg>
            </button>
            <button @click="changeSlide(current + 1)"
                class="absolute right-2 top-1/2 -translate-y-1/2 bg-white/80 hover:bg-white p-2 rounded-full">
                <svg class="w-5 h-5 md:w-6 md:h-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="m9 5 7 7-7 7" />
                </svg>
            </button>

            <!-- Dots -->
            <div class="absolute bottom-3 left-1/2 -translate-x-1/2 flex gap-2">
                <button v-for="(_, i) in slides" @click="current = i"
                    :class="[ 'w-2 h-2 md:w-3 md:h-3 rounded-full transition-all', current === i ? 'bg-white scale-125' : 'bg-white/50' ]" />
            </div>
        </div>
    </div>

    <div class="">
        <AppHero-1-1/>
    </div>
    
</template>
