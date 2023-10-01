<script lang="ts">
const ICONS_PATH = '/images/benefits-icons/';

export interface BenefitItem {
    iconFile: string;
    title: string;
    text1: string;
    text2: string; 
}
</script>

<script setup lang="ts">
defineProps<{
    items: BenefitItem[]
}>();
</script>

<template>
    <div class="benefits-list">
        <div class="benefits-list__headers">
            <div class="benefits-list__header">Бесплатные сервера</div>
            <div class="benefits-list__header">Подписочный сервер</div>
        </div>

        <div class="benefits-list__items">
            <div v-for="item in items" :key="item.iconFile" class="benefit-item">
                <img class="benefit-item__icon" :src="ICONS_PATH + item.iconFile">
                <h3 class="benefit-item__title">{{ item.title }}</h3>
                <div class="benefit-item__text1">{{ item.text1 }}</div>
                <div class="benefit-item__text2">{{ item.text2 }}</div>
            </div>
        </div>
    </div>
</template>

<style lang="scss">
.benefits-list {
    width: 632px;
    margin-bottom: 35px;


    &__headers {
        display: flex;
        margin-bottom: 9px;
    }

    &__header {
        width: 140px;
        height: 23px;
        box-sizing: border-box;
        
        border: 1px solid #310e00;
        
        line-height: 23px;
        text-align: center;
        font-family: Roboto;
        font-size: 12px;
        color: #671D00;
    }

    &__header:first-child {
        margin-left: auto;
        margin-right: 11px;
    }

    &__items {

    }
}

.benefit-item {
    display: flex;
    align-items: center;
    
    height: 74px;
    margin-bottom: 1px;
    box-sizing: border-box;

    border: 1px solid #310e00;
    border-radius: 1px;
    background: rgba(0, 0, 0, 0.55);


    &:last-child {
        margin-bottom: 0;
    }

    &__icon {
        width: 64px;
        height: 64px;

        margin-left: 5px;
        margin-right: 19px;
    }

    &__title, &__text1, &__text2 {
        font-family: Roboto;
        font-size: 16px;
        color: #FFF;
    }

    &__title {
        width: 180px;
        margin: 0;

        font-weight: normal;
    }

    &__text1 {
        width: 72px;
        text-align: center;

        margin-left: auto;
    }

    &__text2 {
        width: 72px;
        text-align: center;

        margin-left: 76px;
        margin-right: 41px;
    }
}
</style>