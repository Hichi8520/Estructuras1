<template>
    <div class="home">
        <h1>{{ msg }}</h1>
        <span>Ingrese el 1er numero    </span>
        <input v-model.number="num1" type="number">
        <p></p>

        <span>Ingrese el 2do numero   </span>
        <input v-model.number="num2" type="number">
        <p></p>

        <span>Sumar   </span>
        <input type="button" @click="sumar" />
        <p>Resultado: {{suma}}</p>

        <span>Restar   </span>
        <input type="button" @click="restar" />
        <p>Resultado: {{resta}}</p>

        <span>Multiplicar   </span>
        <input type="button" @click="multiplicar" />
        <p>Resultado: {{multi}}</p>

        <span>Dividir   </span>
        <input type="button" @click="dividir" />
        <p>Resultado: {{divi}}</p>

    </div>
</template>

<script lang="ts">
    import { Component, Prop, Vue } from 'vue-property-decorator';

    @Component
    export default class Home extends Vue {
        @Prop() private msg!: string;

        suma: number = 0
        resta: number = 0
        multi: number = 0
        divi: number = 0

        num1: number = 0
        num2: number = 0

        sumar() {
            this.suma = 0
            this.suma = this.num1 + this.num2
        }

        restar() {
            this.resta = 0
            this.resta = this.num1 - this.num2
        }

        multiplicar() {
            this.multi = 0
            this.multi = this.num1 * this.num2
        }

        dividir() {
            this.divi = 0
            this.divi = this.num1 / this.num2
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
