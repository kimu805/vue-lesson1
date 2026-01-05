<script setup>
  import { ref } from 'vue';
  import { useRefLimitedHistory } from './composables/refLimitedHistory';

  const count = ref(0)

  const { history, undo  } = useRefLimitedHistory(count, 3)
  const userInput = ref("")
  const { history: history2, undo: undo2 } = useRefLimitedHistory(userInput, 6)

</script>

<template>
  <h1>history</h1>
  <p>count: {{ count }}</p>
  <button @click="count++">increment</button>
  <p>history: {{ history }}</p>
  <button @click="undo">undo</button>

  <h1>history2</h1>
  <p>userInput: {{ userInput }}</p>
  <input v-model="userInput" type="text">
  <p>history2: {{ history2 }}</p>
  <button @click="undo2">undo</button>
</template>