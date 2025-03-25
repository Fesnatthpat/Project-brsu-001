<script setup lang="ts">
import { ref } from "vue"

const slides = [
    { img: "images/1.jpg", text: "welcome" },
    { img: "images/2.jpg", text: "welcome" },
    { img: "images/3.jpg", text: "welcome" },
]

const current = ref(0)
const changeSlide = (i: number) => current.value = (i + slides.length) % slides.length

</script>

<template>
    <!-- Hero Section -->
    <div class="flex justify-center items-center min-h-screen w-full mt-5 lg:mt-0">
        <div class="max-w-[1300px] w-full">
            <div class="grid grid-cols-1 p-4 lg:grid-cols-3 gap-4 w-full">
                <!-- box1 -->
                <div class=" lg:col-span-2 w-full">
                    <div class="flex flex-col gap-y-4">
                        <!-- swiper-con -->
                        <div class=" bg-white w-full rounded-md overflow-hidden h-[450px] relative">
                            <!-- Slide-img -->
                            <div class="max-w-full h-full">
                                <img class="w-full h-full object-cover" :src="slides[ current ].img" alt="">

                            </div>
                            <!-- bg Gradient -->
                            <div
                                class="absolute inset-x-0 bottom-0 h-1/3 bg-gradient-to-t from-[#1c66d6] to-transparent">
                            </div>

                            <!-- Navigation -->
                            <button @click="changeSlide(current - 1)"
                                class="absolute left-2 top-1/2 -translate-y-1/2 bg-white/80 hover:bg-white p-2 rounded-full">
                                <svg class="w-5 h-5 md:w-6 md:h-6" xmlns="http://www.w3.org/2000/svg" fill="none"
                                    viewBox="0 0 24 24">
                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                        stroke-width="2" d="m15 19-7-7 7-7" />
                                </svg>
                            </button>
                            <button @click="changeSlide(current + 1)"
                                class="absolute right-2 top-1/2 -translate-y-1/2 bg-white/80 hover:bg-white p-2 rounded-full">
                                <svg class="w-5 h-5 md:w-6 md:h-6" xmlns="http://www.w3.org/2000/svg" fill="none"
                                    viewBox="0 0 24 24">
                                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round"
                                        stroke-width="2" d="m9 5 7 7-7 7" />
                                </svg>
                            </button>
                        </div>
                        <!-- items-row -->
                        <div class="ring rounded-md w-full h-auto lg:h-[275px]">
                            <div class="m-2">
                                <div class="grid grid-cols-2 gap-3">
                                    <!-- box-items -->
                                    <div v-for="i in 4" :key="i" class=" w-full h-auto lg:h-[120px] rounded-md ring p-1">
                                        <div class="px-2">
                                            <h2>โครงงานคอมพิวเตอร์</h2>
                                        </div>
                                        <div class="mt-10 p-2">
                                            <a class="btn btn-sm btn-primary" href="">ดูทั้งหมด</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <!-- box2 -->
                <div class=" p-4 w-full rounded-md  ring">
                    <div class="flex justify-between items-center mb-3">
                        <div class="">
                            <h2 class="text-[19px] font-bold">โครงงานคอมพิวเตอร์</h2>
                        </div>
                        <div class="">
                            <span class="text-primary underline">ดูทั้งหมด</span>
                        </div>
                    </div>
                    <div class="flex flex-col gap-y-2">
                        <!-- box-items -->
                        <div v-for="i in 7" :key="i" class=" w-full h-[90px] rounded-md ring p-1">
                            <div class="px-2">
                                <h2>โครงงานคอมพิวเตอร์</h2>
                            </div>
                            <div class="mt-3 p-2">
                                <a class="btn btn-sm btn-primary" href="">ดูทั้งหมด</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped></style>