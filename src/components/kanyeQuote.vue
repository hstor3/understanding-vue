<template>
    <kanyeAPI />
</template>

<script>
    import kanyeAPI from '../services/kanyeAPI.vue';

    export default {
        name: 'kanyeComponent',
        components: {
            kanyeAPI
        }
    }
</script>