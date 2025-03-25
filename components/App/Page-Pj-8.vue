<script setup lang="ts">
useHead({
    title: 'ยื่นสอบจบ'
})

</script>

<template>
    <div class="p-2 w-full flex justify-center items-center">
        <!-- bg -->
        <div
            class="bg-gradient-to-t from-[#a9c9fb] to-[#1c66d6] rounded-2xl w-full p-5 lg:max-w-[1500px] h-auto  lg:h-[800px] flex justify-center items-center">
            <!-- box-Project-container -->
            <div class="flex flex-col justify-center items-center w-full">
                <!-- Navbar -->
                <AppNavbar-2 />

                <!-- box-item-PJ -->
                <div
                    class="bg-white relative flex flex-col items-center w-full max-w-[95%] sm:max-w-full md:w-[990px] lg:max-w-[990px] xl:max-w-[1200px] h-auto mt-5 rounded-2xl p-5">
                    <div class="text-[24px] sm:text-[30px] font-bold text-center mt-2">
                        ยื่นสอบจบ</div>
                    <div class="mt-5 w-full">
                        <div class="border border-gray-400 w-full h-auto rounded-[5px] p-4 sm:p-5">
                            <div class="flex flex-col gap-y-3">
                                <div class="text-center text-3xl font-medium">
                                    <h2 class="text-gray-400">ยื่นสอบจบ</h2>
                                    <h2 class="text-gray-400">(ยังไม่มีข้อมูล)</h2>
                                </div>
                                <div class="text-center">
                                    <!-- <div class="btn bg-[#1c66d6] text-white">ขอยื่นสอบหัวข้อ</div> -->
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
/* ซ่อน scrollbar */
::-webkit-scrollbar {
    display: none;
}

/* ซ่อน scrollbar ใน Firefox */
.scrollbar-none {
    -ms-overflow-style: none;
    /* Internet Explorer 10+ */
    scrollbar-width: none;
    /* Firefox */
}
</style>
