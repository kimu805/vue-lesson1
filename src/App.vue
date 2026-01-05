<script setup>
import BaseCard from './components/BaseCard.vue';

</script>

<template>
  <h1>Slots</h1>
  <BaseCard>
    <template #header="{ pageCount }">
      <p>{{ pageCount }}</p>
      <h2 v-if="pageCount === 1">Vue.js Course</h2>
      <h2 v-if="pageCount === 2">HTML Course</h2>
      <h2 v-if="pageCount === 3">CSS Course</h2>
    </template>
    <template #main="{ pageCount }">
      <h2>this is a main</h2>
      <p v-if="pageCount === 1">hello</p>
      <p v-if="pageCount === 2">how are you?</p>
      <p v-if="pageCount === 3">goodbye</p>
    </template>
    <template #footer>
      <h2>this is a footer</h2>
    </template>

  </BaseCard>
</template>