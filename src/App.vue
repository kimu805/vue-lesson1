<script setup>
  import { ref, reactive } from "vue"
  const title = ref("Vue.js Course")
  let price = ref(9.99)

  function increment() {
    price.value += 1
    instructor.bio = "hi"
  }

  const info = ref({
    students: 1000, 
    rating: 4
  })

  const instructor = reactive({
    name: "Kazuto",
    age: 25,
    sns: {
      twitter: "@kazuto",
      youtube: "@kazuto_channel"
    },
    email: ref("kimukimuok805@gmail.com")
  })

  instructor.bio = "hello"
  console.log(instructor.name)
  console.log(info.value.students)

  const courseInfo = {
    sections: ref(10),
    language: ref("japanese")
  }
</script>

<template>
  <h1>Title: {{ title }}</h1>
  <h2>Price: ${{ price - 1 }}</h2>
  <button @click="increment">button</button>
  <h2>Students: {{ info }}</h2>
  <h2>Instructor: {{ instructor.name }}</h2>
  <h2>Instructor Bio: {{ instructor.bio }}</h2>
  <h2>CourseInfo Sections: {{ courseInfo.sections.value }}</h2>
</template>

