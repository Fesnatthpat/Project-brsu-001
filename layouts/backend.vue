<script setup lang="ts">
</script>

<template>
    <div class="flex">
        <!-- Sidebar -->
        <AppSidebar />

        <!-- Main Content Area -->
        <div class="flex-1 flex flex-col min-h-screen">
            <!-- <AppHeader /> -->
            <main class="flex-1 p-4 mt-10 lg:mt-0">
                <slot />
            </main>
        </div>
    </div>
</template>


<style scoped>
/* Add any additional styling if needed */
</style>