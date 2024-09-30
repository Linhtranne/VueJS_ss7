<template>
  <div>
    <h1>Bài 8</h1>
    <button @click="showForm = true">Add User</button>

    <FormAddUser v-if="showForm" @close="closeForm" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import FormAddUser from './Child.vue'

const showForm = ref(false)

const closeForm = () => {
  showForm.value = false
}
</script>
