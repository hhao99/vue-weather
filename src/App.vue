<script setup lang="ts">
import { RouterView } from 'vue-router'
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <div class="container">
    <Header />
  </div>
  <main>
    <RouterView />
  </main>
  <div>
    <Footer />
  </div>
</template>
