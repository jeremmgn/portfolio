<template>
    <div class="overlay" :style="{ left: isOpen ? '0' : '-100%' }">
      <div class="overlay__header">
        <div @click="toggleMenu" class="overlay__icon">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
            <path d="M18 6L6 18M6 6L18 18" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
          </svg>
        </div>
      </div>
      <nav class="overlay__navigation">
        <a @click="toggleMenu" class="overlay__item" href="#">Accueil</a>
        <a @click="toggleMenu" class="overlay__item" href="#about">À propos</a>
        <a @click="toggleMenu" class="overlay__item" href="#project">Projets</a>
        <a @click="toggleMenu" class="overlay__item" href="#contact">Contact</a>
      </nav>
    </div>
      <header class="header">
        <div class="header__container">
          <a class="header__item" href="#">Portfolio.</a>
          <div @click="toggleMenu" class="header__icon">
              <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                  <path d="M3 12H21M3 6H21M3 18H21" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
          </div>
          <nav class="header__navigation">
            <a class="header__item" href="#">Accueil</a>
            <a class="header__item" href="#about">À propos</a>
            <a class="header__item" href="#project">Projets</a>
            <a class="header__item" href="#contact">Contact</a>
          </nav>
        </div>
      </header>
  </template>
  
  <script setup lang="ts">
  import { ref } from 'vue';
  
  const isOpen = ref(false);
  
  const toggleMenu = () => {
    isOpen.value = !isOpen.value;
  };
  </script>
  
  <style scoped lang="scss">
  @import '../style.scss';
  
  .overlay {
    position: fixed;
    left: -100%;
    top: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    background-color: $purple;
    transition: left .4s ease;
    z-index: 1;
    &__header {
      position: fixed;
      width: 100%;
      height: 72px;
      display: flex;
      flex-direction: row;
      justify-content: flex-end;
      align-items: center;
      padding: 0 48px;
    }
    &__icon {
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      & svg {
        color: $white;
      }
      &:hover svg {
        color: $yellow;
      }
    }
    &__navigation {
      margin: auto;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 24px;
    }
      &__item {
      color: $white;
      font-family: $font-family;
      font-size: 48px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      text-decoration: none;
      &:hover {
        color: $yellow;
      }
    }
  
    @media (max-width: 800px) {
      &__item {
        font-size: 36px;
      }
    }
    
    @media (max-width: 600px) {
        &__header {
            height: 48px;
            padding: 0 24px;
        }
        &__icon {
            width: 18px;
            height: 18px;
        }
        & svg {
            width: 18px;
            height: 18px;
        }
    }
  
    @media (max-width: 500px) {
      &__item {
        font-size: 24px;
      }
    }
  }
  
  .header {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: $purple;
    &__container {
      width: 1200px;
      height: 72px;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      padding: 0 48px;
    }
    &__navigation {
      display: flex;
      flex-direction: row;
      justify-content: center;
      align-items: center;
      gap: 24px;
    }
    &__item {
      color: $white;
      font-family: $font-family;
      font-size: 16px;
      font-style: normal;
      font-weight: 700;
      line-height: normal;
      text-decoration: none;
      &:hover {
        color: $yellow;
      }
    }
    &__icon {
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      & svg {
        color: $white;
      }
      &:hover svg {
        color: $yellow;
      }
    }
    
    @media (min-width: 1201px) {
        &__icon {
            display: none;
        }
    }
  
    @media (max-width: 1200px) {
        &__navigation {
            display: none;
        }
    }

    @media (max-width: 1000px) {
        &__item {
            font-size: 16px;
        }
    }
  
    @media (max-width: 600px) {
        &__container {
            height: 48px;
            padding: 0 24px;
        }
        &__icon {
            width: 18px;
            height: 18px;
        }
        & svg {
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