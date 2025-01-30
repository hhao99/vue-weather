<script setup lang="ts">
defineProps<{
  msg: string
}>()
</script>

<template>
  <div class="w-full border-b-2 border-yellow-200 p-4 shadow-lg">
    <h1 class="text-3xl text-center text-yellow-800">{{ msg }}</h1>
  </div>
</template>
