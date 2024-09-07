
<template>
    <h1 class="text-2xl font-bold text-center text-gray-800">Segundo Componente</h1>

    <div class="flex justify-center space-x-4">
    <h3>Número - {{ numero }}</h3>
    <button
      class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 focus:outline-none focus:ring focus:ring-blue-300"
      @click="numero++"
    >+1</button>
    <button
      class="px-4 py-2 bg-red-500 text-white rounded hover:bg-red-600 focus:outline-none focus:ring focus:ring-blue-300"
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


</script>

<style scoped>
h3 {
    color: red;
}
</style>


