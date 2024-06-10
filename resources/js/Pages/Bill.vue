<script setup>
import LeftSideBarLayout from '@/Layouts/LeftSideBarLayout.vue';
import BillLayout from '@/Layouts/BillLayout.vue'
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Счета" />
    <div class="dashboard">
        <LeftSideBarLayout></LeftSideBarLayout>
        <BillLayout></BillLayout>
    </div>
</template>