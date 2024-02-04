<template>
    <section id="about" class="about">
        <div class="about__container">
            <div class="about__header">
                <Heading anchor="#about" heading="À propos" />
                <Subheading subheading="Qui suis-je ? 👨🏼‍💻" />
            </div>
            <div class="about__content">
                <div class="about__wrapper">
                    <div class="about__text">Je suis Jérémy Monguin, étudiant en troisième année de licence à l'Institut Supérieur des Sciences et Techniques de Saint-Quentin et passionné par le développement web sous toutes ses formes, allant de la création de logiciel et d'application jusqu'à la conception de site web ou même de jeu vidéo.</div>
                    <div class="about__text">Au cours de ma formation, j'ai pu développer de solides compétences en algorithmique, en mathématiques et en sciences de l'ingénieur, tout en découvrant divers langages de programmation tels que HTML, CSS et JavaScript. Ma soif d'apprentissage m'a conduit à m'intéresser à des technologies plus modernes telles que TypeScript, Vue.js et Node.js. En parallèle, j'ai enrichi mon expérience en prenant en main des outils de conception tels que Figma, me permettant ainsi de créer des interfaces intuitives et agréables à utiliser.</div>
                </div>
                <div class="about__tech-stack">
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/html.svg)' }"></div>
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/css.svg)' }"></div>
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/js.svg)' }"></div>
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/git.svg)' }"></div>
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/vuejs.svg)' }"></div>
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/nodejs.svg)' }"></div>  
                        <div class="about__icon" :style="{ backgroundImage: 'url(assets/figma.svg)' }"></div>              
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

.about {
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
        padding: 96px 48px 0 48px;
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
        flex-direction: column;
        justify-content: flex-start;
        align-items: center;
        gap: 24px;
    }
    &__wrapper {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: flex-start;
        gap: 12px;
    }
    &__text {
        color: $dark-grey;
        font-family: $font-family;
        font-size: 16px;
        font-style: normal;
        font-weight: 200;
        line-height: normal;
    }
    &__tech-stack {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: flex-end;
        align-items: center;
        gap: 12px;
    }
    &__icon {
        width: 48px;
        height: 48px;
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 50%;
        background-size: cover;
        background-position: center;
        box-shadow: 0px 4px 6px 0px rgba(51, 51, 51, 0.24);
        transition: transform .2s ease;
        &:hover {
            transform: translateY(-4px);
        }
    }

    @media (max-width: 1200px) {
        &__container {
            width: 100%;
        }
    }

    @media (max-width: 1000px) {
        &__text {
            font-size: 15px;
        }
        &__content {
            gap: 24px
        }
        &__tech-stack {
            gap: 8px;
        }
        &__icon {
            width: 36px;
            height: 36px;
            box-shadow: 0px 4px 6px 0px rgba(51, 51, 51, 0.12);
        }
    }

    @media (max-width: 600px) {
        &__container {
            padding: 48px 24px 0 24px;
        }
    }

    @media (max-width: 500px) {
        &__text {
            font-size: 14px;
        }
        &__tech-stack {
            gap: 4px;
        }
        &__icon {
            width: 24px;
            height: 24px;
            box-shadow: 0px 4px 6px 0px rgba(51, 51, 51, 0.06);
        }
    }
}
</style>