<script setup>
import { onMounted } from 'vue'
import ApexCharts from 'apexcharts'

// Sparkline Charts
const initSpark1 = () => {
    new ApexCharts(document.querySelector('#spark1'), {
        chart: { type: 'line', height: 80, sparkline: { enabled: true } },
        series: [ { data: [ 25, 66, 41, 89, 63, 25, 44, 12, 36, 9, 54 ] } ],
        stroke: { curve: 'smooth', width: 2 },
        colors: [ '#3B82F6' ]
    }).render()
}

const initSpark2 = () => {
    new ApexCharts(document.querySelector('#spark2'), {
        chart: { type: 'area', height: 80, sparkline: { enabled: true } },
        series: [ { data: [ 47, 45, 54, 38, 56, 24, 65, 31, 37, 39, 62 ] } ],
        colors: [ '#10B981' ],
        stroke: { curve: 'smooth', width: 2 },
        fill: { opacity: 0.3 }
    }).render()
}

const initSpark3 = () => {
    new ApexCharts(document.querySelector('#spark3'), {
        chart: { type: 'bar', height: 80, sparkline: { enabled: true } },
        series: [ { data: [ 12, 24, 16, 32, 18, 28, 14, 19, 22, 27, 35 ] } ],
        colors: [ '#F59E0B' ]
    }).render()
}

// Bar Chart
const initBarChart = () => {
    new ApexCharts(document.querySelector('#bar'), {
        chart: { type: 'bar', height: 350 },
        series: [ {
            name: 'Sales',
            data: [ 65, 78, 66, 89, 92, 88, 76, 98, 85, 72, 90, 82 ]
        } ],
        xaxis: {
            categories: [ 'Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec' ]
        },
        colors: [ '#3B82F6' ],
        plotOptions: {
            bar: { borderRadius: 4, columnWidth: '45%' }
        }
    }).render()
}

// Donut Chart
const initDonutChart = () => {
    new ApexCharts(document.querySelector('#donut'), {
        chart: { type: 'donut', height: 350 },
        series: [ 44, 55, 13, 33 ],
        labels: [ 'Marketing', 'Development', 'Support', 'Others' ],
        colors: [ '#3B82F6', '#10B981', '#F59E0B', '#EF4444' ],
        legend: { position: 'bottom' },
        plotOptions: {
            pie: { donut: { labels: { show: true, total: { show: true } } } }
        }
    }).render()
}

// Area Chart
const initAreaChart = () => {
    new ApexCharts(document.querySelector('#area'), {
        chart: { type: 'area', height: 350 },
        series: [ {
            name: 'Website Traffic',
            data: [ 3100, 4000, 2800, 5100, 4200, 10900, 1000, 3000, 7500, 4300, 5500, 1500 ]
        } ],
        xaxis: {
            categories: [ '01 Jan', '02 Jan', '03 Jan', '04 Jan', '05 Jan', '06 Jan', '07 Jan', '08 Jan', '09 Jan', '10 Jan', '11 Jan', '12 Jan' ]
        },
        colors: [ '#8B5CF6' ],
        stroke: { curve: 'smooth' },
        fill: {
            type: 'gradient',
            gradient: {
                shadeIntensity: 1,
                opacityFrom: 0.7,
                opacityTo: 0.3
            }
        }
    }).render()
}

// Line Chart
const initLineChart = () => {
    new ApexCharts(document.querySelector('#line'), {
        chart: { type: 'line', height: 350 },
        series: [
            { name: 'Current Year', data: [ 28, 29, 33, 36, 32, 32, 33 ] },
            { name: 'Previous Year', data: [ 12, 11, 30, 18, 25, 30, 22 ] }
        ],
        xaxis: {
            categories: [ 'Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul' ]
        },
        colors: [ '#3B82F6', '#10B981' ],
        stroke: { width: 3, curve: 'smooth' },
        markers: { size: 5 },
        legend: { position: 'top' }
    }).render()
}

onMounted(() => {
    initSpark1()
    initSpark2()
    initSpark3()
    initBarChart()
    initDonutChart()
    initAreaChart()
    initLineChart()
})

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
    <div class="min-h-screen  p-4">
        <div class="container mx-auto">
            <!-- Sparkboxes Grid -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 mb-4">
                <div class=" p-6 rounded-lg shadow-sm border">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-2xl font-bold ">$424,652</p>
                            <p class="text-gray-500">Sales</p>
                        </div>
                        <span class="bg-blue-100 text-blue-800 text-xs font-medium px-2.5 py-0.5 rounded">
                            +53%
                        </span>
                    </div>
                    <div id="spark1" ref="spark1" class="mt-2"></div>
                </div>

                <div class=" p-6 rounded-lg shadow-sm border">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-2xl font-bold ">$235,312</p>
                            <p class="text-gray-500">Expenses</p>
                        </div>
                        <span class="text-xs text-gray-500">07 Sep</span>
                    </div>
                    <div id="spark2" ref="spark2" class="mt-2"></div>
                </div>

                <div class=" p-6 rounded-lg shadow-sm border">
                    <div class="flex justify-between items-start">
                        <div>
                            <p class="text-2xl font-bold ">$135,965</p>
                            <p class="text-gray-500">Profits</p>
                        </div>
                        <span class="text-xs text-gray-500">07 Sep</span>
                    </div>
                    <div id="spark3" ref="spark3" class="mt-2"></div>
                </div>
            </div>

            <!-- ส่วนอื่นๆ ของ template ที่เหลือเหมือนเดิม -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
                <div class=" p-4 rounded-lg shadow-sm border">
                    <div id="bar" ref="bar"></div>
                </div>
                <div class=" p-4 rounded-lg shadow-sm border">
                    <div id="donut" ref="donut"></div>
                </div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                <div class=" p-4 rounded-lg shadow-sm border">
                    <div id="area" ref="area"></div>
                </div>
                <div class=" p-4 rounded-lg shadow-sm border">
                    <div id="line" ref="line"></div>
                </div>
            </div>
        </div>
    </div>
</template>



<style>
/* สามารถเพิ่ม custom styles ได้ที่นี่หากจำเป็น */
</style>