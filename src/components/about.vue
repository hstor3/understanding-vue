<template>
<div class='bg-secondary mt-2 py-2 rounded text-white-50'>
    <p>
      This is a basic Vue App that contains internal CSS (ew, sorry), bootstrap, Vue, JavaScript, and HTML.
      This site uses the 
      <a class='text-decoration-none text-black-50' :href="openWeatherURL" target="_blank">
        Open Weather API
      </a>
      , the 
      <a class='text-decoration-none text-black-50' :href="kanyeRestURL" target='_blank'>
        Kanye Rest API
      </a>
      , and was created to help me quickly learn the VueJs basics.
    </p>
  </div>
</template>

<script>
  export default {
    name: 'aboutSection',
    data() {
      return {
        kanyeRestURL: 'https://kanye.rest/?ref=apitemple',
        openWeatherURL: 'https://openweathermap.org/current'
      }
    }
  }
</script>