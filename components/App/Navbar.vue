<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isOpenMenu = ref(false)

const toggleMenu = () => {
    isOpenMenu.value = !isOpenMenu.value // สลับสถานะเมื่อคลิก
}

const handleClickOutside = (event: MouseEvent) => {
    const menu = document.querySelector('.menu-dropdown')
    const hamburger = document.querySelector('.hamburger-menu')

    if (
        menu &&
        hamburger &&
        !menu.contains(event.target as Node) &&
        !hamburger.contains(event.target as Node)
    ) {
        isOpenMenu.value = false // ซ่อนเมนูถ้าคลิกนอก
    }
}

// ผูกและถอด event listener เมื่อ component ถูก mount/unmount
onMounted(() => {
    document.addEventListener('click', handleClickOutside)
})

onUnmounted(() => {
    document.removeEventListener('click', handleClickOutside)
})
</script>

<template>
    <div class="bg-[#1c66d6] px-[30px] py-2 flex justify-between items-center z-50 border-b-1 border-white sticky top-0">
        <!-- btn-menu (สำหรับ desktop) -->
        <div class="gap-3 hidden lg:flex">
            <NuxtLink to="/" class="btn btn-sm">หน้าหลัก</NuxtLink>
            <NuxtLink to="/Page-Project" class="btn btn-sm">หน้าโครงงาน</NuxtLink>
            <NuxtLink to="/backend/dashboard" class="btn btn-sm">จัดการ</NuxtLink>
            <div class="btn btn-sm">คู่มือการทำบัณฑิตนิพนธ์</div>
            <div class="btn btn-sm">แบบฟอร์มCP</div>
        </div>
        <!-- Menu (Mobile) -->
        <div class="flex lg:hidden relative">
            <!-- icon-Hamburger -->
            <div @click="toggleMenu" class="btn bg-[#1c66d6] border-1 shadow-none cursor-pointer p-2 hamburger-menu">
                <svg class="w-[40px] h-[40px] text-white" aria-hidden="true" xmlns="http://www.w3.org/2000/svg"
                    width="24" height="24" fill="none" viewBox="0 0 24 24">
                    <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M18 6H6m12 4H6m12 4H6m12 4H6" />
                </svg>

                <!-- dropdown -->
                <div v-show="isOpenMenu"
                    class="h-auto w-[200px] rounded-[5px] bg-[#cde1ff] p-2 text-center absolute left-0 top-12 z-50 overflow-hidden transition-all duration-300 ease-in-out menu-dropdown"
                    :class="{ 'max-h-0 opacity-0': !isOpenMenu, 'max-h-[250px] opacity-100': isOpenMenu }">
                    <div class="gap-3 flex flex-col">
                        <NuxtLink to="/" class="btn btn-sm">หน้าหลัก</NuxtLink>
                        <NuxtLink to="/Page-Project" class="btn btn-sm">หน้าโครงงาน</NuxtLink>
                        <NuxtLink to="/backend/dashboard" class="btn btn-sm">จัดการ</NuxtLink>
                        <div class="btn btn-sm">คู่มือการทำบัณฑิตนิพนธ์</div>
                        <div class="btn btn-sm">แบบฟอร์มCP</div>
                    </div>
                </div>
            </div>
        </div>
        <!-- menu-right -->
        <div class="flex items-center gap-[100px]">
            <!-- ช่องค้นหา -->
            <div class="w-[300px] relative hidden">
                <div class="relative">
                    <input
                        class="w-full bg-white rounded-[5.5px] p-2 pr-10 text-black placeholder-gray-500 focus:outline-none"
                        type="text" placeholder="ค้นหา...">
                    <button
                        class="absolute right-0 top-0 h-full bg-[#4285f4] rounded-r-[5px] text-white px-3 flex items-center hover:bg-[#3267d6] transition-colors">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
                        </svg>
                    </button>
                </div>
            </div>
            <!-- profile -->
            <div class="flex items-center gap-[20px]">
                <div class="avatar">
                    <div class="w-[40px] rounded-full">
                        <img src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp" />
                    </div>
                </div>
                <!-- Name -->
                <div class="hidden md:block">
                    <h3 class="text-white">Natthpat Phummek</h3>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/* ไม่ต้องใช้ scoped style เพราะเราใช้ Tailwind เท่านั้น */
</style>