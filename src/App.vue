<script setup>
import { onMounted, useTemplateRef } from 'vue';

const userInput = useTemplateRef("user-input")
console.log(userInput.value)
onMounted(() => {
  userInput.value.focus()
})
</script>

<template>
  <input type="text" ref="user-input">
</template>