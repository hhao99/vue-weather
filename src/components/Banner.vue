<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="w-full border-b-1 border-gray-200 p-4 shadow-sm">
    <h1 class="text-3xl text-center text-blue-800 dark:bg-gray-800 dark:text-blue-200">{{ msg }}</h1>
  </div>
</template>
