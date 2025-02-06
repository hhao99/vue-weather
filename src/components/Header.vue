<template>
  <header class="flex flex-col justify-between w-full h-60 bg-gray-800 text-white">
    <img alt="Vue logo" class="rouned-lg" src="@/assets/logo.svg" width="30" height="30" />

    <div class="flex flex-col justify-between">
      <Banner msg="Weather forecast protect you from bad weather!" />
      <nav class="flex justify-end space-x-4">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/weather">Weather</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>
<script lang="ts" setup>
import { RouterLink } from 'vue-router'
import Banner from '@/components/Banner.vue'
</script>
