<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png" />  -->


      <MostrarTablaDatos
      :titulo="datos2.titulo"
      :datos="datos2.datos"
      :columnas="datos2.columnas"
      :fondo="datos2.fondo"
      :color-titulo="datos2.colorTexto"
    >
    </MostrarTablaDatos>

      <MostrarTablaDatos
      :titulo="datos3.titulo"
      :datos="datos3.datos"
      :columnas="datos3.columnas"
      :fondo="datos3.fondo"
      :color-titulo="datos3.colorTexto"
    >
    </MostrarTablaDatos>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

import MostrarTablaDatos from "./components/MostrarTablaDatos.vue";

export default {
  name: "App",

  components: {
    MostrarTablaDatos
  },
  data() {
    return {
      datos1: {
        columnas: ["ID", "NOMBRE", "SUELDO"],
        titulo: "Planilla Geincos SAC",
        datos: [
          {
            id: 1,

            nombre: "Sergio Jara Mendoza",

            sueldo: 2500,
          },
          {
            id: 2,

            nombre: "Joselo Miranda",

            sueldo: 1800,
          },
          {
            id: 3,

            nombre: "Ricardo Sanchez",

            sueldo: 1500,
          },
        ],
        fondo: {
          "table table-dark": true,
        },
        colorTexto: {
          "text-primary": true,
        },
      },

      datos2: {
        columnas: ["ID", "CURSO", "PRECIO"],
        titulo: "CURSOS",
        datos: [
          {
            id: 1,

            curso: "LARAVEL 8",

            precio: 200,
          },
          {
            id: 2,

            curso: "VUE JS",

            precio: 250,
          },
          {
            id: 3,

            curso: "REACT JS",

            precio: 300,
          },
        ],

        fondo: {
          table: true,
        },
        colorTexto: {
          "text-warning": true,
        },
      },
      datos3: {
        columnas: ["ID", "AREAS"],
        titulo: "AREAS",
        datos: [
          {
            id: 1,

            area: "sistemas",
          },
          {
            id: 2,

            area: "finanzas",
          },
          {
            id: 3,

            area: "logistica",
          },
        ],
        fondo: {
          "table table-striped": true,
        },
        colorTexto: {
          "text-primary": true,
        },
      },
    };
  },
};
</script>
  

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
