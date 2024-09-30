<template>
    <div class="form-container">
      <h2>Add New User</h2>
      <form @submit.prevent="handleSubmit">
        <div>
          <label for="name">Name:</label>
          <input type="text" v-model="name" id="name" required />
        </div>
        <div>
          <label for="email">Email:</label>
          <input type="email" v-model="email" id="email" required />
        </div>
        <div>
          <label for="address">Address:</label>
          <input type="text" v-model="address" id="address" required />
        </div>
        <button type="submit">Add User</button>
        <button type="button" @click="closeForm">Close</button>
      </form>
      
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const name = ref('')
  const email = ref('')
  const address = ref('')
  const handleSubmit = () => {
    alert(`User added: \nName: ${name.value}\nEmail: ${email.value}\nAddress: ${address.value}`)
    name.value = ''
    email.value = ''
    address.value = ''
  }
  const closeForm = () => {
    emit('close')
  }
  </script>
  
  <style scoped>
  .form-container {
    border: 1px solid #ccc;
    padding: 20px;
    margin-top: 20px;
  }
  </style>
  