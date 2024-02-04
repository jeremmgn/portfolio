<template>
    <section id="project" class="project">
        <div class="project__container">
            <div class="project__header">
                <Heading anchor="#project" heading="Projets" />
                <Subheading subheading="Nouvelles créations 🔥" />
            </div>
            <div class="project__content">
                <ProjectCard v-for="project in projects" :image="project.image" :title="project.title" />
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import Heading from './Heading.vue';
import Subheading from './Subheading.vue';
import ProjectCard from './ProjectCard.vue';

const projects = [
    { image: '/assets/code_generator.png', title: 'Générateur automatique de code' },
    { image: '/assets/chess.png', title: 'Jeu d\'échecs' },
    { image: '/assets/asteroids.png', title: 'Asteroids' },
];
</script>

<style scoped lang="scss">
@import '../style.scss';

.project {
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
        display: grid;
        justify-content: flex-start;
        align-items: center;
        grid-template-columns: repeat(auto-fill, 50% 50%);
        grid-gap: 12px;
    }
    
    @media (max-width: 1200px) {
        &__container {
            width: 100%;
        }
    }

    @media (max-width: 1000px) {
        &__content {
            grid-template-columns: repeat(auto-fill, 100%);
        }
    }

    @media (max-width: 600px) {
        &__container {
            padding: 48px 24px 0 24px;
        }
    }

    @media (max-width: 500px) {
        
    }
}
</style>