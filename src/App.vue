<template>
  <div class="container-fluid mt-3">
    <div class="card shadow">
      <header class="card-header app-header">
        <h1>PNT2 - Examen Parcial</h1>
      </header>
      <main class="card-body p-5">
        <ConversorTemperatura /> 
      </main>
    </div>
  </div>
</template>

<script>
import ConversorTemperatura from './components/ConversorTemperatura.vue';

export default {
  name: 'app',
  components: {
    ConversorTemperatura 
  }
}
</script>

<style scoped>
.app-header {
  background-color: #2c3e50; 
  color: white;
  text-align: center;
  padding: 15px;
}
h1 {
  margin-bottom: 0;
  font-size: 1.8rem;
}
</style>
