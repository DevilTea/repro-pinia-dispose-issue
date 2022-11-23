<template>
  <h1>Count: {{ store.count }}</h1>
  <button @click="store.increment">Increment</button>
</template>

<script setup>
import { onUnmounted } from 'vue'
import { useCounterStore } from '@/stores/counter'
const store = useCounterStore()

onUnmounted(() => {
  store.$dispose()
})
</script>
