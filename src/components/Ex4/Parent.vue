<template>
    <div>
        <h1>Bài 4</h1>
        <h2>Parent Component</h2>
      <ul>
        <li v-for="todo in todos" :key="todo.id">
          <TodoItem :todo="todo" @deleteTodo="handleDeleteTodo" />
        </li>
      </ul>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import TodoItem from './Child.vue'

  const todos = ref([
    { id: 1, name: 'he' },
    { id: 2, name: 'hehehe' },
    { id: 3, name: 'hehe' }
  ])
  const handleDeleteTodo = (id) => {
    todos.value = todos.value.filter(todo => todo.id !== id)
  }
  </script>
  