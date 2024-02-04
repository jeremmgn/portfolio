<template>
    <footer id="footer" class="footer">
        <div class="footer__container">
            <Social />
        </div>
    </footer>
</template>

<script setup lang="ts">
import Social from './Social.vue';
</script>

<style scoped lang="scss">
@import '../style.scss';

.footer {
    width: 100%;
    height: 48px;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $purple;
    &__container {
        width: 1200px;
        display: flex;
        justify-content: flex-end;
        align-items: center;
        padding: 0 48px;
    }

    @media (max-width: 1200px) {
        &__container {
            width: 100%;
        }
    }
    
    @media (max-width: 600px) {
        height: 36px;
        
        &__container {
            padding: 0 24px;
        }
    }
}
</style>