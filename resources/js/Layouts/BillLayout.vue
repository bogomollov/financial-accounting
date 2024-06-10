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
                                <div class="bill-card" id="card-orange">
                                    <div class="bill-info">
                                        <div class="up-info">
                                            <div>Дебетовая карта</div>
                                            <img src="../../images/garbage.svg">
                                        </div>
                                        <div class="down-info">
                                            23 750 ₽
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="bill-item">
                                <div class="bill-card" id="card-red">
                                    <div class="bill-info">
                                        <div class="up-info">
                                            <div>Кредитная карта</div>
                                            <img src="../../images/garbage.svg">
                                        </div>
                                        <div class="down-info">
                                            55 000 ₽
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="bill-item">
                                <div class="bill-card" id="card-purple">
                                    <div class="bill-info">
                                        <div class="up-info">
                                            <div>Электронный кошелек</div>
                                            <img src="../../images/garbage.svg">
                                        </div>
                                        <div class="down-info">
                                            5 000 ₽
                                        </div>
                                    </div>
                                </div>
                            </div>
                            <div class="bill-item">
                                <div class="bill-card" id="card-add">
                                    <img src="../../images/plus.svg" width="40" height="40">
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
.bills {
    display: flex;
    gap: 40px;
}
.bill-card {
    background-image: url(../../images/card-mask.png);
    border-radius: 20px;
    width: 326px;
    height: 184px;
}
#card-orange {
    background-color: var(--orange);
}
#card-red {
    background-color: var(--red);
}
#card-purple {
    background-color: var(--purple);
}
#card-add {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid var(--gray);
}
.bill-info {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    padding: 35px 20px;
    height: 100%;
}
.up-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: 500;
    font-size: 20px;
}
.down-info {
    font-size: 24px;
    font-weight: 500;
}
</style>
