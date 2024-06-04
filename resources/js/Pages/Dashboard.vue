<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>

<template>
    <Head title="Домашняя страница" />
    <!-- Имя авторизированного пользователя {{ $page.props.auth.user.name }} -->
    <AuthenticatedLayout>
    </AuthenticatedLayout>
</template>
