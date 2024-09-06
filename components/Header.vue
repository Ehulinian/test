<template>
  <header class="header">
    <div class="container">
      <div class="header__content">
        <NuxtLink to="/">
          <img src="../assets/LOGO.svg" alt="Logo" class="header__logo" />
        </NuxtLink>
        <nav class="nav">
          <ul class="nav__list">
            <li class="nav__item">
              <NuxtLink href="/" class="nav__link">Home</NuxtLink>
            </li>
            <li class="nav__item">
              <NuxtLink href="#about" class="nav__link">About</NuxtLink>
            </li>
            <li class="nav__item">
              <NuxtLink href="#pricing" class="nav__link">Pricing</NuxtLink>
            </li>
            <li class="nav__item">
              <NuxtLink href="#facts" class="nav__link">Facts</NuxtLink>
            </li>
            <li class="nav__item">
              <NuxtLink href="#blog" class="nav__link">Blog</NuxtLink>
            </li>
            <li class="nav__item">
              <NuxtLink href="#support" class="nav__link">Support</NuxtLink>
            </li>
          </ul>
          <div class="header__buttons">
            <button class="header__btn" @click="toggleDownloadMenu">
              Download
            </button>
            <div v-if="showDownloadMenu" class="header__download-menu">
              <NuxtLink
                to="https://apps.apple.com/ua/app/apple-store/id375380948?l=ru"
                class="header__download-link"
                >App Store</NuxtLink
              >
              <NuxtLink
                to="https://play.google.com/store/games?hl=ru&pli=1"
                class="header__download-link"
                >Google Play</NuxtLink
              >
            </div>
            <div class="header__dropdown" @click="toggleLanguageMenu">
              <span class="toogle-language">{{ selectedLanguage }}</span>
              <div class="toogle-language--select">
                <img src="../assets/arrow-down.svg" alt="Toogle" />
              </div>
            </div>
            <div v-if="showLanguageMenu" class="header__language-menu">
              <button @click="setLanguage('Eng')" class="toogle-btn">
                <img
                  src="../assets/united-kingdom (1) 1.svg"
                  alt="UK"
                  class="icon"
                />English
              </button>
              <button @click="setLanguage('Swe')" class="toogle-btn">
                <img
                  src="../assets/sweden 1.svg"
                  alt="SWE"
                  class="icon"
                />Sverige
              </button>
            </div>
          </div>
        </nav>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const selectedLanguage = ref('Eng')
const showLanguageMenu = ref(false)
const showDownloadMenu = ref(false)

const toggleLanguageMenu = () => {
  showLanguageMenu.value = !showLanguageMenu.value
}

const setLanguage = (language) => {
  selectedLanguage.value = language
  showLanguageMenu.value = false
}

const toggleDownloadMenu = () => {
  showDownloadMenu.value = !showDownloadMenu.value
}
</script>

<style lang="scss" scoped>
.header {
  position: relative;
  padding-block: 28px;

  &__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__logo {
    transition: transform 0.3s ease;
    width: 123px;
    height: 49px;
  }

  &__logo:hover {
    transform: scale(1.1);
  }

  &__buttons {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 38px;
    position: relative;
  }

  &__btn {
    width: 174px;
    height: 44px;
    border-radius: 100px;
    background: rgba(103, 80, 164, 1);
    border: none;
    color: rgba(255, 255, 255, 1);
    cursor: pointer;
    transition:
      background-color 0.3s ease,
      transform 0.3s ease;
  }

  &__btn:hover {
    background-color: #0056b3;
    transform: scale(1.05);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
  }

  &__dropdown {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 61px;
    height: 28px;
    transition: transform 0.3s ease;
    cursor: pointer;
  }

  .icon {
    width: 22px;
    height: 22px;
  }

  .toogle-btn {
    border: none;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 14px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
    color: rgba(35, 21, 62, 1);
    cursor: pointer;
    background: none;

    gap: 7px;
  }

  &__dropdown:hover {
    transform: scale(1.2);
  }

  &__download-menu {
    position: absolute;
    bottom: -90px;
    right: 100px;
    width: 174px;
    display: flex;
    flex-direction: column;
    background-color: rgba(255, 255, 255, 1);
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    padding: 10px;
    gap: 10px;
  }

  &__download-link {
    text-decoration: none;
    color: #0056b3;
    font-weight: 500;
    text-align: center;
    font-size: 14px;
    font-weight: 400;
    line-height: 28px;
    text-align: left;
    color: rgba(35, 21, 62, 1);
  }

  &__download-link:hover {
    text-decoration: underline;
  }

  &__language-menu {
    position: absolute;
    top: 40px;
    right: 0px;
    background-color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 10px;
    display: flex;
    flex-direction: column;

    padding: 5px;
  }

  .toogle-language--select {
    width: 24px;
    height: 24px;
  }
}

.container {
  padding-inline: 135px;
}

.nav {
  display: flex;
  gap: 33px;

  &__list {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 24px;
    margin: 0px;
    list-style: none;
    padding: 0px;
  }

  &__link {
    text-decoration: none;
    color: rgba(35, 21, 62, 1);
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    transition:
      color 0.3s ease,
      transform 0.3s ease;
  }

  &__link:hover {
    color: #0056b3;
    transform: scale(1.05);
  }
}
</style>
