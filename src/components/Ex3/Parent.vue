<template>
    <div>
        <h1>Bài 3</h1>
        <h2>Parent Component</h2>
      <p>Current Count: {{ count }}</p>
      <CountChildren @increment="handleIncrement" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import CountChildren from './Child.vue'

  const count = ref(0)
  const handleIncrement = () => {
    count.value++
  }
  </script>
  