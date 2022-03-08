<template>
  <button v-on:click='refresh' class='my-5 btn btn-warning'>New Quote</button>
</template>

<script>
  export default {
    name: 'refreshQuote',
    methods: {
      refresh: function () {
        location.reload()
      }
    }
  } 
</script>