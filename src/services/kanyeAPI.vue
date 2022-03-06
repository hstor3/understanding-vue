<template>
  <div class='my-2'>
  "{{ quote.quote }}"
  </div>
</template>

<script>
export default {
    name: 'kanyeAPI',
  data() {
    return {
      quote: []
    }
  },
  methods: {
    async getData() {
      try {
        let response = await fetch("https://api.kanye.rest");
        this.quote = await response.json();
      } catch (error) {
        console.log(error);
      }
    }
  },
  created() {
    this.getData()
  }
};
</script>