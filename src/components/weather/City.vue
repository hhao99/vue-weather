<script setup lang="ts">
import { ref } from 'vue'
const url = 'https://api.weatherbit.io/v2.0/current'
const apiKey = 'a8e27a3b5a86405995003b245d10bec5'
const city = ref('winnipeg')
const data = ref(null)

const fetchWeather = async () => {
  const uri = `${url}?city=${city.value}&key=${apiKey}`
  const response = await fetch(uri)
  const result = await response.json()
  data.value = result.data[0]
}
</script>
<template>
  <main>
    <div class="w-full p-4 rounded-lg shadow-lg">
      <input
        type="text"
        placeholder="Enter City"
        class="bg-white dark:bg-gray-600 dark:text-white w-full p-2 rounded-lg"
        id="city"
        v-model="city"
        @keypress.enter="fetchWeather"
      />
    </div>

    <div v-if="data">
      <h1>Weather of City: {{ data.city_name }}, {{ data.country_code }}</h1>
      <p>updated at: {{ data.ob_time }}</p>
      <ul>
        <li>Temperature: {{ data.temp }}, feel Like {{ data.app_temp }}</li>
        <li>Pressure: {{ data.pres }}</li>
        <li>Wind speed: {{ data.wind_spd }} m/s.</li>
        <li>Relative Humidity: {{ data.rh }}%.</li>
        <li>Cloud coverate {{ data.clouds }}%.</li>
      </ul>
    </div>
  </main>
</template>
