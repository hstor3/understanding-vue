<template>
  <weatherAPI />
</template>

<script>
  import weatherAPI from '../services/weatherAPI.vue';

  export default {
    name: 'seattleWeather',
    components: {
      weatherAPI
    }
  }
</script>