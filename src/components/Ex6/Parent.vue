<template>
    <div>
        <h1>Bài 6</h1>
      <button @click="openModal">Open Modal</button>

      <Modal :isOpen="isModalOpen" @close="closeModal">
        <template #header>
            Thông tin sản phẩm
        </template>
        <template #body>
          Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lí
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
  
  