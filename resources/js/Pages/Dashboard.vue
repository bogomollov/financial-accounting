<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import LeftbarLayout from '@/Layouts/LeftSideBarLayout.vue';
import DashboardLayout from '@/Layouts/DashboardLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Домашняя страница" />
    <LeftbarLayout></LeftbarLayout>
    <DashboardLayout></DashboardLayout>
    <!-- Имя авторизированного пользователя {{ $page.props.auth.user.name }} -->
    <!-- <AuthenticatedLayout>
    </AuthenticatedLayout> -->
</template>
