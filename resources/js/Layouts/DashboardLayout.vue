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
            <div class="home-content">
                <div class="block-1">
                    <div class="block-border">
                        <div class="balances">
                            <h2>Остаток на счетах</h2>
                            <div class="balances-item">
                                <div class="bal-item bal-amount">
                                    <p>Всего</p>
                                    15 493 ₽
                                </div>
                                <div class="bal-item bal-amount">
                                    <p>Наличные</p>
                                    1 200 ₽
                                </div>
                                <div class="bal-item bal-amount">
                                    <p>Дебетовые карты</p>
                                    5 000 ₽
                                </div>
                                <div class="bal-item bal-amount">
                                    <p>Кредитные карты</p>
                                    7 000 ₽
                                </div>
                                <div class="bal-item bal-amount">
                                    <p>Электронные кошельки</p>
                                    293 ₽
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="block-border">
                        <div class="graph-analytics">
                            <div class="graph-title">
                                <h2>График расходов и доходов</h2>
                            <div class="designation">
                                <div class="income">
                                    <div class="green-circle"></div>
                                    Прибыль
                                </div>
                                <div class="expenses">
                                    <div class="red-circle"></div>
                                    Затраты
                                </div>
                            </div>
                            </div>
                            <div>
                                <img src="../../images/graph.svg">
                            </div>
                        </div>
                    </div>
                </div>
                <div class="block-2">
                    <div class="block-border">
                        <div class="monthly-expenses">
                            <h2>Затраты за этот месяц</h2>
                            <div class="monthly-content">
                                <div class="circle-diagram">
                                    <img src="../../images/circle.svg">
                                </div>
                                <div class="category-expenses">
                                    <div id="transfer" class="item-expenses">
                                        Переводы 550 ₽
                                    </div>
                                    <div id="mobile-network" class="item-expenses">
                                        Связь 2350 ₽
                                    </div>
                                    <div id="stationery" class="item-expenses">
                                        Канцтовары 800 ₽
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                    <div class="block-border">
                        <div class="goals">
                            <h2>Цели</h2>
                            <div class="goals-panel">
                                <div class="goal-item">
                                    <div class="goal-info">
                                        <p>Земельный участок</p>
                                        5 500 000 ₽
                                    </div>
                                    <div class="progress-bar">
                                        <span class="progress-bar-fill" style="width: 50%;"></span>
                                    </div>
                                </div>
                                <div class="goal-item">
                                    <div class="goal-info">
                                        <p>BMW M3</p>
                                        3 200 000 ₽
                                    </div>
                                    <div class="progress-bar">
                                        <span class="progress-bar-fill" style="width: 35%;"></span>
                                    </div>
                                </div>
                                <div class="goal-item">
                                    <div class="goal-info">
                                        <p>Путешествие</p>
                                        1 000 000 ₽
                                    </div>
                                    <div class="progress-bar">
                                        <span class="progress-bar-fill" style="width: 20%;"></span>
                                    </div>
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
    padding: 120px 60px 0px;
    width: 100%;
}
#username {
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    background-image: var(--green-gradient);
    font-weight: 500;
}
.home-title {
    justify-content: space-between;
    align-items: center;
}
.home-content {
    display: flex;
    gap: 30px;
}
.block-border {
    padding: 40px 30px;
    background-color: var(--dark-gray);
    border-radius: 10px;
    height: 100%;
}
.balances {
    display: flex;
    gap: 40px;
    flex-direction: column;
}
.balances-item {
    display: flex;
    gap: 30px;
}
.bal-item {
    display: flex;
    flex-direction: column;
    gap: 15px;
}
.bal-item p {
    color: var(--gray);
    font-weight: 500;
}
.bal-amount {
    font-weight: 500;
}
.block-1 {
    width: 100%;
}
.block-1,
.block-2 {
    display: flex;
    flex-direction: column;
    gap: 30px;
}
.graph-analytics {
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.graph-title {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.designation {
    display: flex;
    gap: 20px;
}
.income, .expenses {
    display: flex;
    align-items: center;
    gap: 10px;
}
.green-circle {
    width: 8px;
    height: 8px;
    background: var(--green);
    border-radius: 50%;
}
.red-circle {
    width: 8px;
    height: 8px;
    background: var(--red);
    border-radius: 50%;
}
.goals {
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.goals-panel {
    display: flex;
    flex-direction: column;
    gap: 30px;
}
.goal-item {
    display: flex;
    flex-direction: column;
    gap: 10px;
    width: 454px;
}
.goal-info {
    display: flex;
    justify-content: space-between;
}
.progress-bar, progress {
    width: 100%;
}
.progress-bar {
    background-color: var(--gray);
    border-radius: 5px;
}
.progress-bar-fill {
    display: block;
    height: 8px;
    background-color: var(--white);
    border-radius: 5px;
}
.monthly-expenses {
    display: flex;
    flex-direction: column;
    gap: 40px;
}
.monthly-content {
    display: flex;
    gap: 30px;
}
.category-expenses {
    display: flex;
    flex-direction: column;
    gap: 15px;
    width: auto;
}
.category-expenses .item-expenses {
    padding: 10px;
    border-radius: 10px;
    font-weight: 500;
    width: max-content;
}
#transfer {
    background-color: var(--yellow);
    color: var(--dark-gray);
}
#mobile-network {
    background-color: var(--blue);
    color: var(--dark-gray); 
}
#stationery {
    background-color: var(--purple);
    color: var(--white); 
}
</style>
