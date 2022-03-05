<template>
    <h2>
        <kanyeAPI />
        <weatherAPI />
    </h2>
</template>

<script>
    import kanyeAPI from '../services/kanyeAPI.vue';
    import weatherAPI from '../services/weatherAPI.vue';

    export default {
        name: 'HomePage',
            components: {
                kanyeAPI,
                weatherAPI
            }
    }
</script>