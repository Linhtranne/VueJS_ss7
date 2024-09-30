<template>
    <div>
      <h2>Product Children</h2>
      <p>Product ID: {{ product.id }}</p>
      <p>Product Name: {{ product.name }}</p>
      <p>Product Price: {{ product.price }}</p>
      <p>Product Quantity: {{ product.quantity }}</p>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    product: {
      type: Object,
      required: true
    }
  })
  </script>
  