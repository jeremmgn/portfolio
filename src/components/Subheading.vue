<template>
    <h2 class="subheading">{{ subheading }}</h2>
</template>

<script setup lang="ts">
defineProps(['subheading']);
</script>

<style scoped lang="scss">
@import '../style.scss';

.subheading {
    color: $black;
    font-family: $font-family;
    font-size: 36px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    
    @media (max-width: 1000px) {
        font-size: 30px;
    }

    @media (max-width: 500px) {
        font-size: 24px;
    }
}
</style>