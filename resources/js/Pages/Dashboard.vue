<script setup>
import LeftSideBarLayout from '@/Layouts/LeftSideBarLayout.vue';
import DashboardLayout from '@/Layouts/DashboardLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Домашняя страница" />
    <div class="dashboard">
        <LeftSideBarLayout></LeftSideBarLayout>
        <DashboardLayout></DashboardLayout>
    </div>
</template>
<style>
    .dashboard {
        display: flex;
    }
</style>