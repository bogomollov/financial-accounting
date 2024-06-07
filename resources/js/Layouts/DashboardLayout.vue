<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
</script>

<template>
    <div class="home">
        <div class="home-wrapper">
            <div class="sm:flex home-title">
                <h1>Добро пожаловать, <span id="username">{{ $page.props.auth.user.name }}</span></h1>
                <AuthenticatedLayout></AuthenticatedLayout>
            </div>
        </div>
    </div>
</template>
<style>
.home {
    display: flex;
    height: 100vh;
    width: 100vw;
    background-color: var(--black);
    color: var(--white);
}
.home-wrapper {
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding-top: 40px;
}
#username {
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    background-image: var(--green-gradient);
    font-weight: 500;
}
</style>
