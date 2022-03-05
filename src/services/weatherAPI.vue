<template>
  <div>
    <img :src="`${this.iconSource}`"/>
  </div>
</template>

<script>
export default {
  name: 'weatherAPI',
  data() {
    return {
      weather: [],
      icon: '',
      iconSource: ''
    }
  },
  methods: {
    async getData() {
      try {
        let name = 'Holland';
        let response = await fetch('https://api.openweathermap.org/data/2.5/weather?q=' + name + `&appid=${process.env.VUE_APP_APIKEY}&units=imperial`);
        this.weather = await response.json();
        this.icon = await this.weather.weather[0].icon
        this.iconSource = 'http://openweathermap.org/img/w/' + `${this.icon}` + '.png'
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