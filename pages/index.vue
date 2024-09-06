<template>
  <div>
    <HeroSection />
    <HowDoesItWork />
    <WhatToDo/>
    <OurBlog />
    <CallToAction />
  </div>
</template>

<script setup>
import WhatToDo from '~/components/WhatToDo.vue';
import CallToAction from '../components/CallToAction.vue';
import HeroSection from '../components/HeroSection.vue';
import HowDoesItWork from '../components/HowDoesItWork.vue';
import OurBlog from '../components/OurBlog.vue';
</script>
