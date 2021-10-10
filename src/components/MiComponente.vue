<template>
  <div>
    <h1>{{titulo}} </h1>
    <h2> {{subtitulo}} </h2>

    <input v-model="numero_1" type="number" placeholder="numero 1"/>
    <br>
    <input v-model="numero_2" type="number" placeholder="numero 2"/>
    <br>
    <button v-on:click="sumar">Sumar</button>
    <span>Suma: {{resultado}}</span>

    <button v-on:click="restar">Restar</button>
    <span>Resta: {{resultado2}}</span>

    <button v-on:click="multiplicar">Multiplicar</button>
    <span>Multiplicacion: {{resultado3}}</span>

    <button v-on:click="dividir">Dividir</button>
    <span>resultado: {{resultado4}}</span>
<!----Desarrollo los requerimientos para sumar, restar, multiplicar y  dividir-->
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
            resultado: '',
            resultado2: '', 
            resultado3: '',
            resultado4: '',
        };
    },
    methods:{
        sumar(){
            this.resultado = parseInt(this.numero_1) + parseInt(this.numero_2);
        },
        restar(){
            this.resultado2 = parseInt(this.numero_1) - parseInt(this.numero_2);
        },
        multiplicar(){
            this.resultado3 = parseInt(this.numero_1) * parseInt(this.numero_2);
        },
        dividir(){
            this.resultado4 = parseInt(this.numero_1) / parseInt(this.numero_2);
        },
    },
};
</script>

<style>

</style>