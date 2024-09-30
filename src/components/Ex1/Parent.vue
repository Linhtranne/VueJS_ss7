<template>
    <div>
        <h1>Bài 1</h1>
      <h2>Parent Component</h2>
      <h2>Parent Company: {{ parentData }}</h2>
      <ChildrenComponent :propName="parentData" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import ChildrenComponent from './Child.vue'
  const parentData = ref('Rikkei Academy')
  </script>
  