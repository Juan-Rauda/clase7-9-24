<template>
  <h1>Primer componente</h1>
  <h1 class="text-3xl font-bold underline">Hello world!</h1>
  <section>
    <h3>Número - {{ numeroCalculado }}</h3>
  </section>
  <button class="btn" @click="incrementar">+1</button>
  <button class="btn" @click="decrementar">-1</button>
  <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"></button>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue'

const numero = ref(0)

const numeroCalculado = computed(() => {
  return `El número actual es: ${numero.value}`
})

const incrementar = () => {
  numero.value++
}

const decrementar = () => {
  numero.value--
}
</script>

<style scoped>
h1 {
  margin-left: 5px;
}
h3 {
  color: red;
  margin-left: 5px;
}
</style>
