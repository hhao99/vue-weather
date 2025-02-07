<template>
  <header class="flex mb-4 border-b-2 border-gray-200">
    <img alt="Vue logo" class="m-4 rounded-full" src="@/assets/logo.svg" width="30" height="30" />
    <Banner msg="Weather Forecast!" />
    <div class="flex justify-between">
      <nav class="flex justify-end items-end space-x-4">
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
