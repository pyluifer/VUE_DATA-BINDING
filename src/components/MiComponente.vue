<template>
  <div>
    <h1>{{titulo}} </h1>
    <h2> {{subtitulo}} </h2>

    <input v-model="numero_1" type="number" placeholder="numero 1"/>
    <br>
    <input v-model="numero_2" type="number" placeholder="numero 2"/>
    <br>
    <button v-on:click="sumar">Sumar</button>
    <br>
    <span>resultado: {{resultado}}</span>

  </div>
</template>

<script>
export default {
    // Data contiene las variables globales del componente
    data: () =>{
        return {
            titulo:"Titulo Componente",
            subtitulo:"Subtitulo Componente",
            numero_1: null,
            numero_2: null,
            resultado: '' 
        };
    },
    methods:{
        sumar(){
            console.log(this.numero_1);
            this.resultado = parseInt(this.numero_1) + parseInt(this.numero_2);
        }
    },
};
</script>

<style>

</style>