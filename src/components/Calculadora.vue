<template>
<div class="container">
    <h1>{{ result }}</h1>

    <div class="inputs">
            <input v-model="number1" type="number" id="input1">
            <input v-model="number2" type="number" id="input2">
        </div>

    <div class="buttons_cont">
        <div class="buttons">
            <button @click="sumar">➕</button>
            <button @click="restar">➖</button>
        </div>

        <div class="buttons2">
            <button @click="multiplicar">✖️</button>
            <button @click="dividir">➗</button>
        </div>
    </div> 
    </div>

</template>

<script lang="ts">
import { ref } from 'vue'

export default{
data(){
    return{
        number1 : ref <number>(0),
        number2 : ref <number>(0),
        resultCotainer: ref <number>(0),
        result : ref <number>(0)
    }
},

methods:{
    sumar(){
        this.result = this.number1 + this.number2
    },
    restar(){
        this.result = this.number1 - this.number2
    },
    multiplicar(){
        this.result = this.number1 * this.number2
    },
    dividir(){
        this.result = this.number1 / this.number2
    }
},

}
</script>

<style scoped lang="scss">
@import "Calculadora.scss";
</style>