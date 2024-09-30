<template>
    <div>
        <h1>Bài 2</h1>
      <ProductChildren :product="product" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import ProductChildren from './Child.vue'

  const product = ref({
    id: 1,
    name: 'Bưởi ba roi',
    price: 12000,
    quantity: 10
  })
  </script>
  