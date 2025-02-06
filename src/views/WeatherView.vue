<template>
  <div class="flex flex-col justify-center items-center h-screen">
    <h1 class="text-red-800 text-3xl">This is Weather page</h1>
    <WeatherApp />
  </div>
</template>

<script setup lang="ts">
import WeatherApp from '@/components/weather/index.vue'
</script>
