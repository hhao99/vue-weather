<template>
  <header class="flex flex-col justify-between">
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <Banner msg="Weather forecast protect you from bad weather!" />

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
</template>
<script lang="ts" setup>
import { RouterLink } from 'vue-router'
import Banner from '@/components/Banner.vue'
</script>
