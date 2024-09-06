<template>
  <div>
    <Loader v-if="isLoading" /> <!-- Лоадер показується під час завантаження -->
    <NuxtRouteAnnouncer />
    <Header />
    <NuxtPage />
    <Footer />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import { useRouter } from 'vue-router';
import Footer from '~/components/Footer.vue';
import Header from '~/components/Header.vue';
import Loader from '~/components/Loader.vue';

const isLoading = ref(false)
const router = useRouter()

router.beforeEach((to, from, next) => {
  isLoading.value = true
  next()
})

router.afterEach(() => {
  setTimeout(() => {
    isLoading.value = false
  }, 500)
})
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap');

body {
  margin: 0;
}

html {
  height: 100vh;
  font-family: 'Montserrat', sans-serif;
  scroll-behavior: smooth;
  box-sizing: border-box;
}
</style>
