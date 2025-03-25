<script setup>
const students = [
    { id: "6521207013", name: "ณัฐภัทร ภูมิเมฆ", project: "ระบบบริหารจัดการโครงงาน", status: "ผ่าน" },
    { id: "6620107018", name: "Hart Hagerty", project: "Desktop Support", status: "ไม่ผ่าน" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "ผ่าน" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "ไม่ผ่าน" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
    { id: "6720313015", name: "Brice Swyre", project: "Tax Accountant", status: "รอตรวจสอบ" },
];

const statusColor = (status) => {
    return status === "ผ่าน" ? "text-green-500" : status === "ไม่ผ่าน" ? "text-red-500" : "text-yellow-500";
};

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
    <div class="container mx-auto p-4 mt-10 lg:mt-0">
        <div class="overflow-auto rounded-lg border border-gray-300 bg-white shadow-md">
            <table class="min-w-full border-collapse">
                <thead>
                    <tr class="bg-gray-200 text-gray-700">
                        <th class="px-4 py-2 text-left">#</th>
                        <th class="px-4 py-2 text-left">รหัส</th>
                        <th class="px-4 py-2 text-left hidden md:table-cell">ชื่อ-นามสกุล</th>
                        <th class="px-4 py-2 text-left hidden lg:table-cell">ชื่อโครงงาน</th>
                        <th class="px-4 py-2 text-left">สถานะ</th>
                    </tr>
                </thead>
                <tbody>
                    <tr v-for="(student, index) in students" :key="index" class="border-t text-gray-600">
                        <td class="px-4 py-2">{{ index + 1 }}</td>
                        <td class="px-4 py-2">{{ student.id }}</td>
                        <td class="px-4 py-2 hidden md:table-cell">{{ student.name }}</td>
                        <td class="px-4 py-2 hidden lg:table-cell">{{ student.project }}</td>
                        <td class="px-4 py-2" :class="statusColor(student.status)">{{ student.status }}</td>
                    </tr>
                </tbody>
            </table>
        </div>

        <!-- Responsive List for Small Screens -->
        <div class="md:hidden mt-4">
            <div v-for="(student, index) in students" :key="index" class="border p-3 mb-2 rounded-lg shadow-sm">
                <p class="font-bold text-gray-700">#{{ index + 1 }} - {{ student.id }}</p>
                <p class="text-gray-600">{{ student.name }}</p>
                <p class="text-sm text-gray-500">โครงงาน: {{ student.project }}</p>
                <p class="font-semibold" :class="statusColor(student.status)">สถานะ: {{ student.status }}</p>
            </div>
        </div>
    </div>
</template>

