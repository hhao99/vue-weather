<script lang="ts" setup>
  defineProps({
    data: {}
    });
</script>
<template>
<div class="container w-full h-4/5 bg-gray-200 dark:bg-gray-800 dark:text-whitel">
  <div  v-if="data">
    <div class="grid grid-cols-2 gap-x-4">
      <div>
        <h3 class="text-lg text-gray-600">Weather of City: </h3>
        <h1 class="text-3xl text-blue-600 text-center">{{ data.city_name }}, {{ data.country_code }}</h1>
        <h3 class="text-sm text-gray-400 text-right">updated at: {{ data.ob_time }}</h3>
      </div>
      <div class="grid grid-cols-2">
        <h3>Temperature:</h3> <h3>{{ data.temp }} C</h3>
        <h3>Feel Like: </h3> <h3>{{ data.app_temp }} C</h3>
        <h3>Air Pressure:</h3> <h3>{{ data.pres }} Pa.</h3>
        <h3>Wind Speed: </h3> <h3>{{ data.wind_spd}} m/s</h3>
        <h3>Relative Humidity: </h3> <h3>{{ data.rh }}</h3>
        <h3>Cloud coverage: </h3> <h3>{{ data.clouds }}</h3>
      </div>
    </div>
  </div>
</div>
</template>
