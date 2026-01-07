<script setup>
  import { useCounterStore } from '@/stores/counter';
  
  const counterStore = useCounterStore()
  
</script>

<template>
  <h2>CounterComp</h2>
  <button @click="counterStore.count++">increment</button>
  <p>{{ counterStore.count }}</p>
</template>