<script setup>
import { ref, onMounted } from 'vue'

const contador = ref(0)

function incrementarContador() {
  contador.value++
}
function decrementarContador() {
  if(contador.value > 0) {
      contador.value--;
    }
}
function zerarContador() {
  contador.value = 0;
}
onMounted(() => {
  console.log(`O valor inicial do contador é ${contador.value}.`)
})
</script>

<template>
  <h1>{{ contador }}</h1>
  <button @click="incrementarContador">Incrementar</button>
  <button @click="decrementarContador">Decrementar</button>
  <button @click="zerarContador">Zerar</button>
</template>

<style scoped>
button {
  font-weight: bold;
  border: 0;
  margin: 2px;
  padding: 20px;
}
</style>