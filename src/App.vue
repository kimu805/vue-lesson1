<script setup>
import { ref } from 'vue';

  const userInput = ref("")
  const message = ref("")
  const checked = ref("not checked")
  const fruits = ref([])
  const gender = ref("male")
  const selected = ref([])
</script>

<template>
  <h1>v-model</h1>
  <h2>Text</h2>
  <input v-model.lazy.number="userInput" type="text">
  <p>{{ userInput }}</p>

  <h2>Textarea</h2>
  <textarea v-model.trim="message" ></textarea>
  <p style="white-space: pre;">{{ message }}</p>

  <h2>Checkbox</h2>
  <input id="checkbox" v-model="checked" type="checkbox" true-value="checked" false-value="not checked">
  <label for="checkbox">{{ checked }}</label>
  <p>Fruits</p>
  <input type="checkbox" id="apple" v-model="fruits" value="apple" />
  <label for="apple">Apple</label>
  <input type="checkbox" id="banana" v-model="fruits" value="banana" />
  <label for="banana">Banana</label>
  <input type="checkbox" id="grape" v-model="fruits" value="grape" />
  <label for="grape">Grape</label>
  <p>{{ fruits }}</p>

  <h2>Radio Buttons</h2>
  <input v-model="gender" id="male" type="radio" value="male">
  <label for="male">male</label>
  <input v-model="gender" id="female" type="radio" value="female">
  <label for="female">female</label>
  <p>{{ gender }}</p>

  <h2>Select</h2>
  <select v-model="selected" multiple>
    <option value="" disabled>Select one</option>
    <option v-for="option in ['A', 'B', 'C']" :key="option">{{ option }}</option>
  </select>
  <p>{{ selected }}</p>
</template>