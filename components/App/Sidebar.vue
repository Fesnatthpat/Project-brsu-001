<script setup lang="ts">
import { ref } from 'vue';

const isOpen = ref(false); // ควบคุมการเปิด/ปิดเมนูมือถือ

const toggleMenu = () => {
    isOpen.value = !isOpen.value;
};
</script>

<template>
    <!-- ปุ่มเปิดเมนู (เฉพาะมือถือ) -->
    <button @click="toggleMenu" class="lg:hidden fixed top-4 left-4 z-5 bg-blue-600 text-white px-4 py-2 rounded">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"
            class="size-6">
            <path stroke-linecap="round" stroke-linejoin="round" d="M3.75 6.75h16.5M3.75 12H12m-8.25 5.25h16.5" />
        </svg>
    </button>

    <!-- Sidebar (แสดงเฉพาะเดสก์ท็อป) -->
    <aside class="hidden lg:block bg-gradient-to-t from-[#a9c9fb] to-[#1c66d6] border text-white w-64 min-h-screen p-4">
        <nav class="space-y-4">
            <!-- Profile -->
            <div class="flex items-center space-x-3">
                <div class="bg-white w-[40px] h-[40px] rounded-full"></div>
                <div>
                    <h2>Natthpat Phummek</h2>
                </div>
            </div>

            <hr>

            <div>
                <NuxtLink to="/" class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    หน้าหลัก
                </NuxtLink>
                <NuxtLink to="/backend/dashboard"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    Dashboard
                </NuxtLink>
                <NuxtLink to="/backend/projects"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    โครงงาน
                </NuxtLink>
                <NuxtLink to="/backend/Listofnames"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    รายชื่อนักศึกษา
                </NuxtLink>

                <!-- ปุ่ม Logout -->
                <button @click=""
                    class="block w-full text-left text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    Logout
                </button>
            </div>
        </nav>
    </aside>

    <!-- เมนู Sidebar (เฉพาะมือถือ) -->
    <aside
        class="lg:hidden fixed top-0 left-0 bg-gradient-to-t from-[#a9c9fb] to-[#1c66d6] border text-white w-64 min-h-screen p-4 transform transition-transform duration-300 ease-in-out z-40"
        :class="isOpen ? 'translate-x-0' : '-translate-x-full'">
        <nav class="space-y-4">
            <!-- ปุ่มปิดเมนู -->
            <button @click="toggleMenu" class="text-white text-lg absolute top-4 right-4">
                ✖
            </button>

            <!-- Profile -->
            <div class="flex items-center space-x-3">
                <div class="bg-white w-[40px] h-[40px] rounded-full"></div>
                <div>
                    <h2>Natthpat Phummek</h2>
                </div>
            </div>

            <hr>

            <div>
                <NuxtLink to="/" class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    หน้าหลัก
                </NuxtLink>
                <NuxtLink to="/backend/dashboard"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    Dashboard
                </NuxtLink>
                <NuxtLink to="/backend/projects"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    โครงงาน
                </NuxtLink>
                <NuxtLink to="/backend/Listofnames"
                    class="block text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    รายชื่อนักศึกษา
                </NuxtLink>

                <!-- ปุ่ม Logout -->
                <button @click=""
                    class="block w-full text-left text-lg font-semibold hover:bg-gray-100 hover:text-black p-2 rounded">
                    Logout
                </button>
            </div>
        </nav>
    </aside>
</template>
