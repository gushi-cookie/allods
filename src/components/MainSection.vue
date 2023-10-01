<script setup lang="ts">
import BenefitsList from './BenefitsList.vue';
import type { BenefitItem } from './BenefitsList.vue';


let items: BenefitItem[] = [
    {
        iconFile: 'hourglass.png',
        title: 'Игровое время',
        text1: '-',
        text2: '30 дней',
    },
    {
        iconFile: 'spares.png',
        title: 'Запечатанный набор инструментов',
        text1: '1',
        text2: '1',
    },
    {
        iconFile: 'rune.png',
        title: 'Хрупкая чистая руна 10-й ступени',
        text1: '1',
        text2: '-',
    },
    {
        iconFile: 'fire-rune.png',
        title: 'Большой символ изобилия творца',
        text1: '10',
        text2: '-',
    },
    {
        iconFile: 'manna-battery.png',
        title: 'Мана-батарея',
        text1: '-',
        text2: '20',
    },
    {
        iconFile: 'memory-module.png',
        title: 'Модуль памяти',
        text1: '-',
        text2: '10',
    },
    {
        iconFile: 'vito.png',
        title: 'Помощник Вито',
        text1: '1',
        text2: '1',
    },
];
</script>

<template>
    <section class="main-section">
        <div class="main-section__img-container">
            <div class="main-section__circle"></div>
            <img class="main-section__vito" src="/images/main-section_vito.png">
        </div>

        <div class="main-section__right-container">
            <h2 class=main-section__header>Набор «Посылка с контрабандой»</h2>
            <BenefitsList :items="items" />

            <div class="main-section__product">
                <img class="main-section__box" src="/images/main-section_box.png">
                <div class="main-section__purchase">
                    <div class="main-section__price">399 ₽</div>
                    <div class="main-section__purchase-btn">Приобрести</div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss">
.main-section {
    display: flex;
    height: 1060px;

    background:
    url("/images/blue-glow1.png") bottom center no-repeat,
    url("/images/main-section_bg.png") 0 / cover;


    &__img-container {
        position: relative;

        width: 650px;
        margin-left: auto;
    }

    &__circle {
        position: absolute;
        top: 213px;
        right: 55px;

        width: 680px;
        height: 686px;
        
        border: 1px solid #000;
        border-radius: 686px;

        opacity: 0.2;
        mix-blend-mode: lighten;
        filter: blur(100px);
        background-color: #416DF4;
    }

    &__vito {
        position: absolute;
        top: 101px;
        right: 183px;

        width: 354px;
    }


    &__right-container {
        width: 632px;
        margin-right: auto;
    }


    &__header {
        height: 44px;
        margin: 58px 0 35px 0;

        color: #416DF4;
        font-family: "Roboto Condensed";
        font-size: 30px;
        text-transform: uppercase;
    }



    &__product {
        display: flex;
    }

    &__box {
        width: 224px;
        margin-right: 39px;
    }

    &__purchase {
        margin-top: 141px;
    }

    &__price {
        margin-bottom: 12px;

        color: #FFF;
        font-size: 50px;
        font-family: Roboto;
    }

    &__purchase-btn {
        width: 180px;
        height: 40px;
        
        cursor: pointer;
        user-select: none;
        transition: 0.2s;
        text-align: center;
        
        text-transform: uppercase;
        line-height: 40px;
        font-family: Roboto;
        font-size: 16px;

        background-color: #FCFF00;
        border-radius: 7px;

        &:hover {
            background-color: #c7c900;
        }

        &:active {
            background-color: #929408;
        }
    }
}
</style>