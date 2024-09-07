
<template>
    <h1 class="text-2xl font-bold text-center text-gray-800">Primer Componente</h1>

    <div class="flex justify-center space-x-4">
    <h3>Número - {{ numero }}</h3>
    <button
      class="btn"
      @click="numero++"
    >+1</button>
    <button
      class="btn"
      @click="numero--"
    >-1</button>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'

interface Props {
    value: number;
}

const props = defineProps<Props>();

const numero = ref(props.value);

// Creamos una variable reactiva para el número
//const numero = ref(0)
</script>

<style scoped>
h3 {
    color: red;
}
</style>


