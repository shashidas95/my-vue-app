<template>
  <input type="text" v-model="course.name" />
  <h1>{{ course.name }}</h1>
  <input type="text" v-model="course.mentor" />
  <h1>course by: {{ course.mentor }}</h1>
  <input type="text" v-model="course.platform" />
  <h1>platform {{ course.platform }}</h1>
  <div>
    <div><input type="text" v-model="count" /></div>

    <button @click="count++">+</button>
    <h1>{{ count }}</h1>
    <button @click="count--">-</button>
  </div>
</template>

<script setup>
import { ref, reactive } from 'vue'
let count = ref(0)
count.value = 10
let course = reactive({
  name: 'vue js masterclass',
  mentor: 'shashi',
  platform: 'online',
})
course.name = 'vue js 3 masterclass'
</script>
