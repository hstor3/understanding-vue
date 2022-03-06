<template>
  <div class='h-25 mb-2 bg-warning text-white rounded'>
    <h3 class='weather-container py-3'>
      <weatherAPI />
    </h3>
  </div>
</template>

<script>
  import weatherAPI from '../services/weatherAPI.vue';

  export default {
    name: 'chicagoWeather',
    components: {
      weatherAPI
    }
  }
</script>

<style>
  .weather-container {
    transform: translate(0%, 15%);
  }
</style>