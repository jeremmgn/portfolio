<template>
    <section id="home" class="home">
        <div class="home__container">
            <div class="home__content">
                <div class="home__heading">Développeur <span class="home__heading--effect">Full</span> <br> <span class="home__heading--effect">Stack</span> en devenir 👋🏼</div>
                <div class="home__subheading">Bienvenue sur mon portfolio ! Je suis Jérémy Monguin, un étudiant passionné par le développement web et situé à Saint-Quentin, en France. 🇫🇷</div>
                <Social />
            </div>
            <div class="home__image"></div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Social from './Social.vue';
</script>


<style scoped lang="scss">
@import '../style.scss';

.home {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $purple;
    &__container {
        width: 1200px;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        padding: 0 48px;
        gap: 96px;
    }
    &__content {
        width: 565px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 12px;
    }
    &__heading {
        color: $white;
        font-family: $font-family;
        font-size: 60px;
        font-style: normal;
        font-weight: 700;
        line-height: normal;
    }
    &__heading--effect {
        color: $yellow;
    }
    &__subheading {
        color: $light-grey;
        font-family: $font-family;
        font-size: 16px;
        font-style: normal;
        font-weight: 200;
        line-height: normal;
    }
    &__social {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 6px;
    }
    &__link {
        width: 24px;
        height: 24px;
        display: flex;
        justify-content: center;
        align-items: center;
        color: $white;
        &:hover {
            color: $yellow;
        }
    }
    &__image {
        width: 300px;
        height: 300px;
        background-image: url(assets/rocket.png);
        background-position: center;
        background-size: cover;
        border-radius: 50%;
    }
    @media (max-width: 1200px) {
        &__container {
            width: 100%;
            flex-direction: column-reverse;
            padding: 0 48px;
            gap: 24px;
        }
        &__content {
            align-items: center;
        }
        &__heading {
            text-align: center;
        }
        &__subheading {
            text-align: center;
        }
    }

    @media (max-width: 1000px) {
        &__content {
            width: 100%;
        }
        &__heading {
            font-size: 48px;
        }
        &__subheading {
            font-size: 15px;
        }
        &__image {
            width: 250px;
            height: 250px;
        }
    }

    @media (max-width: 600px) {
        &__container {
            padding: 0 24px;
        }
        &__link {
            width: 18px;
            height: 18px;
        }
    }

    @media (max-width: 500px) {
        &__content {
            gap: 9px;
        }
        &__heading {
            font-size: 36px;
        }
        &__subheading {
            font-size: 14px;
        }
        &__image {
            width: 200px;
            height: 200px;
        }
    }
}
</style>