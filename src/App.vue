<template>
  <div>
    <h1>{{ contador }}</h1>
    <button @click="incrementarContador">Incrementar</button>
    <button @click="decrementarContador">Decrementar</button>
  </div>
</template>

<script setup>
  import { ref } from 'vue';
  
  const contador = ref(0);
  
  function incrementarContador() {
    contador.value++;
  }
  
  function decrementarContador() {
    if (contador.value > 0) {
      contador.value--;
    }
  }
</script>
