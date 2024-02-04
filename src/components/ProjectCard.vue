<template>
    <div class="project-card">
        <div :style="{ backgroundImage: `url(${image})` }" class="project-card__image"></div>
        <div class="project-card__title">{{ title }}</div>
    </div>
</template>

<script setup lang="ts">
defineProps(['image', 'title']);
</script>

<style scoped lang="scss">
@import '../style.scss';

.project-card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 6px;
    overflow: hidden;
    &__image {
        width: 100%;
        height: 240px;
        background-size: cover;
        background-position: 50% 0%;
        border-radius: 24px;
        transition: background-position 1.2s ease-in-out;
        &:hover {
            background-position: 50% 100%;
        }
    }
    &__title {
        color: $dark-grey;
        font-family: $font-family;
        font-size: 14px;
        font-style: italic;
        font-weight: 200;
        line-height: normal;
    }

    @media (max-width: 1000px) {
        &__title {
            font-size: 13px;
        }
    }

    @media (max-width: 500px) {
        &__title {
            font-size: 12px;
        }
    }
}
</style>