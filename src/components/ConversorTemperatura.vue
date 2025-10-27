<template>
  <div class="container mt-5 p-4 border rounded shadow-sm">
    <h1 class="text-center mb-4 text-primary">Conversor de Temperatura</h1>

    <div class="form-group mb-4">
      <label for="temp-c" class="font-weight-bold">Ingrese Temperatura °C</label>
      <input 
        id="temp-c"
        type="number" 
        v-model.number="celsius" 
        placeholder="Ingrese °C (ej: -10, 0, 14, 20)"
        class="form-control form-control-lg"
      />
    </div>

    <div class="results-container p-3 border rounded">
      <p :style="{ color: tempColor }" class="result-text">
        **Conv Temperatura °F:** {{ fahrenheit }}
      </p>
      <p :style="{ color: tempColor }" class="result-text">
        **Conv Temperatura °K:** {{ kelvin }}
      </p>
    </div>

    <RespuestasExamen/> 

  </div>
</template>

<script>
import RespuestasExamen from './RespuestasExamen.vue'; 

export default {
  name: 'ConversorTemperatura',
  components: {
    RespuestasExamen
  },
  data() {
    return {
      celsius: 0
    };
  },
  computed: {
    celsiusValue() {
      return Number(this.celsius) || 0;
    },
    
    fahrenheit() {
      return (this.celsiusValue * 9 / 5 + 32).toFixed(2);
    },
    
    kelvin() {
     
      return (this.celsiusValue + 273.15).toFixed(2);
    },
    
    tempColor() {
      if (this.celsiusValue <= 0) {
        return "blue";
      } else if (this.celsiusValue < 15) { 
        return "magenta";
      } else { 
        return "red";
      }
    }
  }
};
</script>