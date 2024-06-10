<script setup>
import LeftSideBarLayout from '@/Layouts/LeftSideBarLayout.vue';
import HistoryTransactionLayout from '@/Layouts/HistoryTransactionLayout.vue'
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="История операций" />
    <div class="dashboard">
        <LeftSideBarLayout></LeftSideBarLayout>
        <HistoryTransactionLayout></HistoryTransactionLayout>
    </div>
</template>