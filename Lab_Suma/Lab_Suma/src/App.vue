<template>
    <div id="app">
        <Home msg="Suma de dos numeros" />
    </div>
</template>

<script lang="ts">
    import { Component, Vue } from 'vue-property-decorator';
    import Home from './components/Home.vue';

    @Component({
        components: {
            Home
        }
    })
    export default class App extends Vue { }
</script>

<style>
</style>
