<template>
    <div>
      <span>{{ todo.name }}</span>
      <button @click="emitDelete">Delete</button>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    todo: {
      type: Object,
      required: true
    }
  })

  const emit = defineEmits(['deleteTodo'])

  const emitDelete = () => {
    emit('deleteTodo', props.todo.id)
  }
  </script>
  