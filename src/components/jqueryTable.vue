<template>
  <div>
      <h2>Tabla de Puertos</h2>
      <table class="table" id="datatable">
        <thead>
          <tr>
            <th>ID</th>
            <th>Nombre</th>
            <th>Pais</th>
            <th>Continente</th>
            <th>Coordenadas</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in puertos" :key="item.id">
            <td>{{item.id}}</td>
            <td>{{item.name}}</td>
            <td>{{item.country}}</td>
            <td>{{item.continent}}</td>
            <td>{{item.coordinates}}</td>
          </tr>
          
        </tbody>
      </table>    
  </div>
</template>
 
<script>
import 'jquery/dist/jquery.min.js';
import 'bootstrap/dist/css/bootstrap.min.css';
import "datatables.net-dt/js/dataTables.dataTables"
import "datatables.net-dt/css/jquery.dataTables.min.css"
import axios from 'axios';
import $ from 'jquery'; 

export default {
  mounted(){
    axios.get("http://apitest.cargofive.com/api/ports").then((response)=>
    {
      this.puertos = response.data;
      $('#datatable').DataTable();
    })
  },
  data: function() {
        return {
            puertos:[]
        }
    },
}
</script>