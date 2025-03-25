<script setup lang="ts">

definePageMeta({
    layout: 'backend',
})

useHead({
    title: 'Dashboard',
    meta: [
        {
            name: 'keywords',
            content: 'Dashboard, Nuxt 3, Backend'
        },
        {
            name: 'Description',
            content: 'Dashboard Nuxt 3,  IT Genius Engineering'
        }
    ]
})

</script>

<template>
    <div class="m-5">
        <!-- ระบบแสดงภาพรวมโครงงานคอมพิวเตอร์ -->
        <div class="text-center">
            <h2 class="text-[25px] font-bold">ระบบแสดงภาพรวมโครงงานคอมพิวเตอร์</h2>
        </div>
        <!-- Itemscontainer-Projects -->
        <div class="mt-10">
            <!-- select -->
            <div class="space-x-3 flex flex-wrap gap-3">
                <select class="border border-[#1c66d6] rounded-md px-5 py-2">
                    <option>ปีการศึกษา</option>
                    <option>2565</option>
                    <option>2566</option>
                    <option>2567</option>
                </select>
                <select class="border border-[#1c66d6] rounded-md px-5 py-2">
                    <option>สถานะ</option>
                    <option>ผ่านแล้ว</option>
                    <option>ไม่ผ่าน</option>
                </select>
            </div>
            <!-- Box-items-container -->
            <div class="mt-5 grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-3">
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
                <!-- item -->
                <div class="border border-[#1c66d6] rounded-md p-3 flex flex-col gap-2">
                    <span>ชื่อโครงงาน : ระบบบริหารจัดการโครงงาน</span>
                    <span>ชื่อผู้วิจัย : นายณัฐภัทร ภูมิเมฆ</span>
                    <span>ชื่ออาจารย์ทีปรึกษา : ดร.เกษม ตริตระการ</span>
                    <div class="flex justify-between items-center mt-auto">
                        <span>12 ก.พ 2568 0432 น</span>
                        <div class="flex items-center gap-2">
                            <div class="w-2 h-2 bg-[#1c66d6] rounded-full"></div>
                            <select class="border border-[#1c66d6] rounded-md px-2 py-1 text-sm">
                                <option>กำลังดำเนินการ</option>
                                <option>สอบหัวข้อไม่ผ่าน</option>
                                <option>เสร็จสมบูรณ์</option>
                            </select>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@media (max-width: 640px) {
    .space-x-3 {
        flex-direction: column;
    }
    .grid-cols-3 {
        grid-template-columns: 1fr;
    }
}
</style>
