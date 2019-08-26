<template>
    <div class="home">
        <h1>{{ msg }}</h1>
        <span>Ingrese el 1er numero    </span>
        <input v-model.number="num1" type="number">
        <p></p>

        <span>Ingrese el 2do numero   </span>
        <input v-model.number="num2" type="number">
        <p></p>

        <span>Operar   </span>
        <input type="button" @click="operar" />
        <p>Suma: {{suma}}</p>

    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component
    export default class Home extends Vue {
        @Prop() private msg!: string;

        suma: number = 0
        num1: number = 0
        num2: number = 0

        operar() {
            this.suma = 0
            this.suma += this.num1 + this.num2
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
