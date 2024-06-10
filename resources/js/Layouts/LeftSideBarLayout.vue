<script setup>
import { Link } from '@inertiajs/vue3';
</script>

<template>
    <div class="menu">
        <div class="menu-wrapper">
            <h2 class="menu-title">Меню</h2>
            <div class="menu-items">
                <Link :href="route('dashboard')" class="menu-item text-item">Домашняя страница</Link>
                <Link :href="route('history')" class="menu-item text-item">История операций</Link>
                <Link :href="route('bill')" class="menu-item text-item">Счета</Link>
            </div>
        </div>
    </div>
</template>
<style>
.menu {
    display: flex;
    height: 100vh;
    width: 300px;
    background-color: var(--dark-gray);
    color: var(--white);
}
.menu-wrapper {
    display: flex;
    flex-direction: column;
    gap: 40px;
    width: inherit;
    padding-top: 50px;
}
.menu-items {
    display: flex;
    flex-direction: column;
}
.menu-items a {
    text-decoration: none;
    color: var(--white);
}
.menu-item {
    padding: 15px 0px;
}
.text-item, .menu-title {
    padding-left: 40px;
}
.menu-item:hover {
    background: var(--gray-gradient);
    transition: 3s;
}
</style>
