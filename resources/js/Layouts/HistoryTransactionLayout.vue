<script setup>
import AuthenticatedLayout from '@/Layouts/AuthenticatedLayout.vue';
</script>

<template>
    <div class="home">
        <div class="home-wrapper">
            <div class="sm:flex home-title">
                <h1>История операций</h1>
                <AuthenticatedLayout></AuthenticatedLayout>
            </div>
            <div class="home-content">
                <div class="block-1">
                    <div class="block-border">
                        <div class="history">
                            <div class="history-column">
                                <p>Название операции</p>
                                <div>Цифровые товары</div>
                                <div>Канцтовары товары</div>
                                <div>Перевод от Богдан Б.</div>
                                <div>Связь</div>
                                <div>Топливо</div>
                                <div>Перевод Денису Т.</div>
                                <div>Цифровые товары</div>
                                <div>Канцтовары товары</div>
                            </div>
                            <div class="history-column">
                                <p>Имя счета</p>
                                <div>Дебетовая карта</div>
                                <div>Кредитная карта</div>
                                <div>Дебетовая карта</div>
                                <div>Дебетовая карта</div>
                                <div>Дебетовая карта</div>
                                <div>Кредитная карта</div>
                                <div>Дебетовая карта</div>
                                <div>Дебетовая карта</div>
                            </div>
                            <div class="history-column">
                                <p>Тип операции</p>
                                <div>Снятие</div>
                                <div>Снятие</div>
                                <div>Пополнение</div>
                                <div>Снятие</div>
                                <div>Снятие</div>
                                <div>Снятие</div>
                                <div>Снятие</div>
                                <div>Снятие</div>
                            </div>
                            <div class="history-column">
                                <p>Изменение баланса</p>
                                <div>-1449,5 ₽</div>
                                <div>-1449,5 ₽</div>
                                <div>+575 ₽</div>
                                <div>-300 ₽</div>
                                <div>-1200 ₽</div>
                                <div>-349 ₽</div>
                                <div>-670 ₽</div>
                                <div>-1000 ₽</div>
                            </div>
                            <div class="history-column">
                                <p>Дата / Время</p>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                                <div>8 Aug 2020,02:45 Am</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<style>
.history {
    display: flex;
    justify-content: space-between;
    gap: 60px;
}
.history-column {
    display: flex;
    flex-direction: column;
    gap: 30px;
}
.history-column p {
    color: var(--gray);
    font-weight: 500;
}
.history-column div {
    font-weight: 500;
}
</style>