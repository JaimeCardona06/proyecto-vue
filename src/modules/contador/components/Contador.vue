<template>
  <h1>Hola mundo</h1>
  <p>{{ contador }}</p>
  <button @click="incrementar()">Incrementar</button>
  <button @click="decrementar()">Decrementar</button>
</template>

<script setup>
  //ref es para trabajar con componentes reactivos
  import { ref } from "vue";

  const contador = ref(0);

  const incrementar = () => {
    //.value sirve para obtener o cambiar el valor de una variable reactiva
    contador.value++;
  }

  const decrementar = () =>{
    contador.value--;
  }

</script>
  
<style scoped>
  p{
    color: red;
  }
</style>
