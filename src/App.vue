<script setup>
import { ref } from 'vue'
const contador = ref (10)

function incrementar (){
  contador.value++
}
function decrementar(){
  if (contador.value > 0)
  contador.value--
}
function reset(){
  contador.value = 0
}
</script>

<template>
  <button @click="decrementar">-</button>
  <button @click="incrementar">+</button>
  <button @click="reset">c</button>
  <p>Valor do contador: {{  contador }}</p>
</template>

<style scoped>
button {
  margin-left: 10px;
  background-color: brown;
  color: black;
  border: none;
  border-radius: 5px;
  padding: 5px 10px;
  cursor: pointer;  
}</style>
 