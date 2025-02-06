<script setup lang="ts">
import { ref } from 'vue'
const url = 'https://api.weatherbit.io/v2.0/current'
const apiKey = 'a8e27a3b5a86405995003b245d10bec5'

const data = ref(null)

const fetchWeather = async () => {
  console.log('fetching weather')
  const options = {
    method: 'GET',
    mode: 'no-cors',
  }
  const response = await fetch(`${url}?city=winnipeg&key=${apiKey}`)
  const result = await response.json()
  data.value = result.data[0]
}
</script>
<template>
  <main>
    <h1>City</h1>
    <button @click="fetchWeather">Get Weather</button>
    <div v-if="data">
      <h1>Weather of City: {{ data.city_name }}</h1>
      <p>Temperature: {{ data.app_temp }}</p>
    </div>
  </main>
</template>
