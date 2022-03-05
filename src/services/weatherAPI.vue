<template>
  <div>
  {{ weather.weather }}
  </div>
</template>

<script>
export default {
  name: 'weatherAPI',
  data() {
    return {
      weather: []
    }
  },
  methods: {
    async getData() {
      try {
        let name = 'Holland';
        let response = await fetch('https://api.openweathermap.org/data/2.5/weather?q=' + name + `&appid=${process.env.VUE_APP_APIKEY}&units=imperial`);
        this.weather = await response.json();
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