<template>
  <div class="container">
    <h1 :class="colorTitulo">{{ titulo }}</h1>
    <table :class="fondo">
    <tr>
        <th v-for="columna  in columnas"  :key="columna.id" scope="col">{{ columna }}</th>
    </tr>

     <tr v-for="dato  in datos" :key="dato.id">
        <td v-for="info  in dato" :key="info.id">{{ info }}</td>
     </tr>
    </table>
  </div>
</template>

<script>
export default {
  name: "MostrarTablaDatos",
 

   props: {
    titulo: String,
    datos: Array,
    columnas:Array,
    fondo: Object,
    colorTitulo: Object
    }

}
</script>

<style lang="scss" >

</style>
