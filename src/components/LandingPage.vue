<template>
    <div class="landing-page">
        <Header />
        <Home />
    </div>
</template>

<script setup lang="ts">
import Header from './Header.vue';
import Home from './Home.vue';
</script>

<style scoped lang="scss">
@import '../style.scss';

.landing-page {
    width: 100%;
    height: 100svh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: $purple;
    overflow: hidden;
}
</style>