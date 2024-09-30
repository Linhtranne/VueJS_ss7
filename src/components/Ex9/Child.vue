<template>
    <button
      :type="type"
      @click="handleClick"
      class="base-button"
    >
      <slot></slot>
    </button>
  </template>
  
  <script setup>
  import { defineProps, defineEmits } from 'vue'

  const props = defineProps({
    type: {
      type: String,
      default: 'button'
    }
  })

  const emit = defineEmits(['click'])

  const handleClick = (event) => {
    emit('click', event)
  }
  </script>
  
  <style scoped>
  .base-button {
    background-color: #4CAF50;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 16px;
  }
  
  .base-button:hover {
    background-color: #45a049;
  }
  </style>
  