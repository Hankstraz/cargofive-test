<template>
  <img alt="Cargofive logo" src="./assets/cargologo.jpg">
  

  <div class="container mt-4">
    <JqueryTable/>
  </div>
</template>

<script>
import JqueryTable from './components/jqueryTable.vue'

export default {
  name: 'App',
  components: {
    
    JqueryTable
  }
}
</script>

<style>
.container {
    max-width: 1000px;
  }
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
