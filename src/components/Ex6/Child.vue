<template>
    <div v-if="isOpen" class="modal-overlay">
      <div class="modal">
        <div class="modal-header">
          <slot name="header"></slot>
        </div>

        <div class="modal-body">
          <slot name="body"></slot>
        </div>

        <div class="modal-footer">
          <button @click="closeModal">Xem chi tiết</button>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const props = defineProps({
    isOpen: {
      type: Boolean,
      required: true
    }
  })

  const emit = defineEmits(['close'])

  const closeModal = () => {
    emit('close')
  }
  </script>
  <style scoped>
  .modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: rgba(0, 0, 0, 0.5);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .modal {
    background: white;
    padding: 20px;
    border-radius: 8px;
    width: 300px;
    max-width: 90%;
  }
  
  .modal-header {
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .modal-body {
    margin-bottom: 20px;
  }
  
  .modal-footer {
    text-align: right;
  }
  </style>
  