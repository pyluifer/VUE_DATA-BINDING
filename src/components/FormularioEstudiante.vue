<template>
  <div>
      <h1>Estudiante</h1>
      <input type="text" v-model="nombre" placeholder="Nombre"/>
      <br>
      <input type="text" v-model="apellido" placeholder="Apellido"/>
      <br>
      <input type="text" v-model="cedula" placeholder="Cedula" />
      <br>
      <button v-on:click="registrar" >Registrar</button>
      <br>
      <br>
      <input v-model="buscar_cedula" type="text" />
      <button v-on:click="buscar">Buscar</button>
      <br>
      <br>
      <table>
          <tr>
              <th>Nombre</th>
              <th>Apellido</th>
              <th>Cedula</th>
          </tr>
          <tr v-for="obj in estudiantes" :key="obj.cedula">
              <td>{{obj.nombre}}</td>
              <td>{{obj.apellido}}</td>
              <td>{{obj.cedula}}</td>
          </tr>
      </table>
    </div>
</template>

<script>
export default {
    data: () =>{
        return{
            nombre: null,
            apellido: null,
            cedula: null,
            estudiantes: [],
            buscar_cedula: null
        }
    },
    methods:{
        registrar(){
            let objEstudiante = {
                nombre: this.nombre,
                apellido: this.apellido,
                cedula: this.cedula
            };
            this.estudiantes.push(objEstudiante);
            console.log(this.estudiantes);
        },
        buscar(){
            let result = this.estudiantes.filter(obj =>(obj.cedula == this.buscar_cedula));
            console.log(result);
        }
    }
};
</script>

<style>
table{
    width: 100%;
}
table,tr,th,td{
    border: 1px solid black;
}
</style>