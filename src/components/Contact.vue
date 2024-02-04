<template>
    <section id="contact" class="contact">
        <div class="contact__container">
            <div class="contact__header">
                <Heading anchor="#contact" heading="Contact" />
                <Subheading subheading="Ne soyez pas timide ! 👇🏼" />
            </div>
            <div class="contact__content">
                <div class="contact__wrapper">
                    <div class="contact__icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                            <path d="M12 13C13.6569 13 15 11.6569 15 10C15 8.34315 13.6569 7 12 7C10.3431 7 9 8.34315 9 10C9 11.6569 10.3431 13 12 13Z" stroke="#FFF" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                            <path d="M12 22C16 18 20 14.4183 20 10C20 5.58172 16.4183 2 12 2C7.58172 2 4 5.58172 4 10C4 14.4183 8 18 12 22Z" stroke="#FFF" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <a class="contact__item" href="https://maps.app.goo.gl/45tRDNenHYvcULpm7" target="_blank">Saint-Quentin, France</a>
                </div>
                <div class="contact__wrapper">
                    <div class="contact__icon">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                            <path d="M2 7L10.1649 12.7154C10.8261 13.1783 11.1567 13.4097 11.5163 13.4993C11.8339 13.5785 12.1661 13.5785 12.4837 13.4993C12.8433 13.4097 13.1739 13.1783 13.8351 12.7154L22 7M6.8 20H17.2C18.8802 20 19.7202 20 20.362 19.673C20.9265 19.3854 21.3854 18.9265 21.673 18.362C22 17.7202 22 16.8802 22 15.2V8.8C22 7.11984 22 6.27976 21.673 5.63803C21.3854 5.07354 20.9265 4.6146 20.362 4.32698C19.7202 4 18.8802 4 17.2 4H6.8C5.11984 4 4.27976 4 3.63803 4.32698C3.07354 4.6146 2.6146 5.07354 2.32698 5.63803C2 6.27976 2 7.11984 2 8.8V15.2C2 16.8802 2 17.7202 2.32698 18.362C2.6146 18.9265 3.07354 19.3854 3.63803 19.673C4.27976 20 5.11984 20 6.8 20Z" stroke="#FFF" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"/>
                        </svg>
                    </div>
                    <a class="contact__item" href="mailto:monguin.jeremy@gmail.com">monguin.jeremy@gmail.com</a>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Heading from './Heading.vue';
import Subheading from './Subheading.vue';
</script>

<style scoped lang="scss">
@import '../style.scss';

.contact {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    &__container {
        width: 1200px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        padding: 96px 48px 96px 48px;
        gap: 24px;
    }
    &__header {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 4px;
    }
    &__content {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: flex-start;
        align-items: center;
        gap: 48px;
    }
    &__wrapper {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 12px;
    }
    &__icon {
        width: 48px;
        height: 48px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: $purple;
        border-radius: 50%;
        box-shadow: 0px 4px 6px 0px rgba(51, 51, 51, 0.24);
    }
    &__item {
        color: $dark-grey;
        font-family: $font-family;
        font-size: 16px;
        font-style: normal;
        font-weight: 200;
        line-height: normal;
        text-decoration: none;
        &:hover {
            color: $purple;
        }
    }

    @media (max-width: 1200px) {
        &__container {
            width: 100%;
        }
    }

    @media (max-width: 1000px) {
        &__item {
            font-size: 15px;
        }
    }

    @media (max-width: 600px) {
        &__container {
            padding: 48px 24px 48px 24px;
        }
        &__content {
            flex-direction: column;
            justify-content: center;
            align-items: flex-start;
            gap: 12px;
        }
        &__icon {
            width: 36px;
            height: 36px;
            box-shadow: 0px 4px 6px 0px rgba(51, 51, 51, 0.12);
        }
        svg {
            width: 18px;
            height: 18px;
        }
    }

    @media (max-width: 500px) {
        &__item {
            font-size: 14px;
        }
    }
}
</style>