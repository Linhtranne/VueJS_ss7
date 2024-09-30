<template>
    <div>
      <h1>Bài 9</h1>
    <BaseButton @click="handleButtonClick">
    Button
      </BaseButton>
    <BaseButton @click="handleButtonSubmit">
        Submit
          </BaseButton>
    <BaseButton @click="handleButtonReset">
        Reset
        </BaseButton>
    </div>
  </template>
  
  <script setup>
  import BaseButton from './Child.vue'
  
  const handleButtonClick = () => {
    alert('He')
  }
  const handleButtonSubmit = () => {
    alert('Submit')
  }
  const handleButtonReset = () => {
    alert('Reset')
  }
  </script>
  
  <style scoped>
  h1 {
    margin-bottom: 20px;
  }
  </style>
  