<template>
  <div class='bg-dark text-white rounded'>
    <h3 class='quote-container h-100'>
      <div class='text-danger'>Quotes by Kanye:</div>
      <kanyeAPI />
      <refreshQuote />
    </h3>
  </div>
</template>

<script>
  import kanyeAPI from '../services/kanyeAPI.vue';
  import refreshQuote from '../common/quoteChange.vue';

  export default {
    name: 'kanyeComponent',
    components: {
      kanyeAPI,
      refreshQuote
    }
  }
</script>

<style>
  .quote-container {
    padding-top: 10%;
    z-index: -1;
  }
</style>