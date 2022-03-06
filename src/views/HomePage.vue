<template>
  <div>
    <button class='btn border' @click="showHideBtn = !showHideBtn">{{showHideBtn ? 'HIDE ABOUT' : 'SHOW ABOUT'}}</button>
  </div>
  <chicagoWeather />
  <kanyeComponent />
  <aboutSection :class="showHideBtn ? 'p-1' : 'd-none'" />
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
        showHideBtn: false
      }
    }
  }
</script>