<template>
  <div>Weather for: {{weather.name}}, IL</div>
  <div>{{this.currentTemp}}˚</div>
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
      iconSource: '',
      currentTemp: ''
    }
  },
  methods: {
    async getData() {
      try {
        let name = 'Chicago';
        let response = await fetch('https://api.openweathermap.org/data/2.5/weather?q=' + name + `&appid=${process.env.VUE_APP_APIKEY}&units=imperial`);
        this.weather = await response.json();
        this.icon = this.weather.weather[0].icon;
        this.iconSource = 'http://openweathermap.org/img/w/' + `${this.icon}` + '.png';
        this.currentTemp = Math.round(this.weather.main.temp);
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