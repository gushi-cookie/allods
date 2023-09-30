<template>
    <section class="head-section">
        <div class="head-section__glow"></div>
        <a class="head-section__logo" href="#"></a>
        <a class="head-section__product" href="#"></a>
        <div class="head-section__info">
            <h1>Коллекционное издание</h1>
            <p>Побеждайте легко, побеждайте стильно с новыми коллекционными изданиями «Аллодов Онлайн»!</p>
        </div>
    </section>
</template>

<style lang="scss">
.head-section {
    position: relative;
    height: 892px;
    overflow-x: hidden;

    background:
    url("/images/blue-glow1.png") bottom center no-repeat,
    url("/images/head-section_gradient-bottom.png") bottom / auto 172px repeat-x,
    url("/images/head-section_char1.png") left bottom / 577px no-repeat,
    url("/images/head-section_char2.png") right bottom / 678px no-repeat,
    url("/images/head-section_gradient-left.png") left top / 462px repeat-y,
    url("/images/head-section_gradient-right.png") right top / 462px repeat-y,
    url("/images/head-section_bg.png") 0px -67.5px / 100% no-repeat;


    &__glow {
        position: absolute;

        width: 100%;
        height: 100%;

        mix-blend-mode: screen;
        background: url("/images/head-section_glow.png") center top / 2150px no-repeat,
    }

    &__logo {
        position: absolute;
        top: 20px;
        left: 0;
        right: 0;
        margin: 0 auto;

        display: block;
        width: 277px;
        height: 236px;

        background-image: url("/images/logo.png");
        background-size: 100%;
    }

    &__product {
        position: absolute;
        top: 258px;
        left: 0;
        right: 0;
        margin: 0 auto;

        display: block;
        width: 695px;
        height: 458px;

        background: url("/images/boxes.png") left top / 667px no-repeat;
    }

    &__info {
        position: absolute;
        left: 0;
        right: 0;
        bottom: 60px;
        margin: 0 auto;

        color: #FFF;
        text-align: center;

        h1 {
            font-family: "Roboto Condensed";
            font-size: 42px;
            font-weight: 700;
            text-transform: uppercase;
            line-height: 44px;

            margin: 0;
            margin-bottom: 25px;
        }

        p {
            font-family: Roboto;
            font-size: 20px;

            margin: 0;
        }
    }
}
</style>