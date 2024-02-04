<template>
    <a :href="anchor" class="heading">{{ heading }}</a>
</template>

<script setup lang="ts">
defineProps(['anchor', 'heading']);
</script>

<style scoped lang="scss">
@import '../style.scss';

.heading {
    color: $purple;
    font-family: $font-family;
    font-size: 18px;
    font-style: normal;
    font-weight: 700;
    line-height: normal;
    text-decoration: none;
    border-left: 6px solid $purple;
    padding: 6px 12px;

    @media (max-width: 1000px) {
        font-size: 16px;
    }

    @media (max-width: 500px) {
        font-size: 14px;
        padding: 4px 8px;
    }
}
</style>