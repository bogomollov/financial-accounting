<script setup>
</script>

<template>
    <div class="menu">
        <div class="menu-wrapper">
            <h2>Меню</h2>
            <div class="menu-items">
                <div class="menu-item text-item">Домашняя страница</div>
                <div class="menu-item text-item">История операций</div>
                <div class="menu-item text-item">Задолженности</div>
                <div class="menu-item text-item">Счета</div>
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
    padding-top: 40px;
}
.menu-items {
    display: flex;
    flex-direction: column;
}
.menu-item {
    padding: 15px 0px;
}
.text-item, h2 {
    padding-left: 40px;
}
.menu-item:hover {
    background: var(--gray-gradient);
    transition: 3s;
}
</style>
