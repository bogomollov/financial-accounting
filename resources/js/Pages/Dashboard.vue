<script setup>
import LeftbarLayout from '@/Layouts/LeftSideBarLayout.vue';
import DashboardLayout from '@/Layouts/DashboardLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Домашняя страница" />
    <div class="sm:flex">
        <LeftbarLayout></LeftbarLayout>
        <DashboardLayout></DashboardLayout>
    </div>
</template>
