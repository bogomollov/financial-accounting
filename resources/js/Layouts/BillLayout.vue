<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
</script>

<template>
<div class="home">
        <div class="home-wrapper">
            <div class="sm:flex home-title">
                <h1>Счета</h1>
                <AuthenticatedLayout></AuthenticatedLayout>
            </div>
            <div class="home-content">
                <div class="block-1">
                    <div class="block-border">
                        <div class="bills">
                            <div class="bill-item">
                                <div class="bill-card">
                                    <img src="../../images/card-mask.png">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.bill-card {
    background-color: var(--orange);
    border-radius: 20px;
    width: 326px;
    height: 184px;
}
</style>
