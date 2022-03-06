<template>
  <div class='mb-2 btn-group-lg border rounded bg-light'>
    <button 
      :class="toggleWeatherBtn ? toggleTrue : toggleFalse" 
      @click="toggleWeatherBtn = !toggleWeatherBtn"
    >
      {{toggleWeatherBtn ? 'HIDE WEATHER' : 'SHOW WEATHER'}}
    </button>
    <button 
      :class="toggleKanyeBtn ? toggleTrue : toggleFalse"
      @click="toggleKanyeBtn = !toggleKanyeBtn"
    >
      {{toggleKanyeBtn ? 'HIDE KANYE' : 'SHOW KANYE'}}
    </button>
    <button 
      :class="toggleAboutBtn ? toggleTrue : toggleFalse"
      @click="toggleAboutBtn = !toggleAboutBtn"
    >
      {{toggleAboutBtn ? 'HIDE ABOUT' : 'SHOW ABOUT'}}
    </button>
  </div>
  <chicagoWeather :class="toggleWeatherBtn ? '' : 'd-none'" />
  <kanyeComponent :class="toggleKanyeBtn ? '' : 'd-none'" />
  <aboutSection :class="toggleAboutBtn ? '' : 'd-none'" />
</template>

<script>
  import kanyeComponent from '../components/kanyeQuote.vue';
  import chicagoWeather from '../components/chicagoWeather.vue';
  import aboutSection from '../components/about.vue';

  export default {
    name: 'HomePage',
    components: {
      kanyeComponent,
      chicagoWeather,
      aboutSection
    },
    data() {
      return {
        toggleAboutBtn: true,
        toggleKanyeBtn: true,
        toggleWeatherBtn: true,
        toggleTrue: 'btn opacity-25',
        toggleFalse: 'btn opacity-75'
      }
    }
  }
</script>