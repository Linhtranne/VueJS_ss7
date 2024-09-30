<template>
    <div>
        <h1>Bài 5</h1>
      <button @click="openModal">Open Modal</button>

      <Modal :isOpen="isModalOpen" @close="closeModal">
        <template #header>
          Thông báo từ hệ thống
        </template>
        <template #body>
          Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.
        </template>
      </Modal>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  import Modal from './Child.vue'

  const isModalOpen = ref(false)

  const openModal = () => {
    isModalOpen.value = true
  }

  const closeModal = () => {
    isModalOpen.value = false
  }
  </script>
  
  