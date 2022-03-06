<template>
  <kanyeComponent />
  <seattleWeather />
</template>

<script>
  import kanyeComponent from '../components/kanyeQuote.vue';
  import seattleWeather from '../components/seattleWeather.vue';

  export default {
    name: 'HomePage',
    components: {
      kanyeComponent,
      seattleWeather
    }
  }
</script>