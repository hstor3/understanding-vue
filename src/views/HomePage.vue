<template>
  <chicagoWeather />
  <kanyeComponent />
  <div>
    <button class='btn border' :class="{toggle: !toggle}" v-on:click='toggleAbout'>{{this.toggle === false ? 'SHOW' : 'HIDE'}}</button>
  </div>
  <aboutSection />
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
        toggle: false
      }
    },
    methods: {
      toggleAbout: function toggleAbout() {
        this.toggle ? true : false
      }
    }
  }
</script>