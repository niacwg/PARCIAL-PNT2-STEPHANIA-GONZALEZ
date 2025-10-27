<template>
  <section class="card mt-4 shadow-sm">
    <div class="card-header bg-primary text-white custom-header">
      <h2 class="mb-0">Respuestas del Examen</h2>
    </div>

    <div class="card-body">
      <p class="respuesta-parcial">
        Respuestas: 1: c - 2: c - 3: a
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'RespuestasExamen',
}
</script>

<style scoped>
.custom-header {
  background-color: #3f51b5;
  color: white;
  padding: 10px 15px;
}

h2 {
  font-size: 1.25rem;
}

.respuesta-final {
  font-weight: bold; 
  color: #d32f2f;
  padding: 10px;
  border: 1px dashed #ccc;
  background-color: #f5f5f5;
  text-align: center; 
}


</style>
