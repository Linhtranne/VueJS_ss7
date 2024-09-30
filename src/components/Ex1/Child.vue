<template>
    <div>
      <h2>Children Component</h2>
      <h2>Children Company  : {{ props.propName }}</h2>
    </div>
  </template>
  
  <script setup>
  const props = defineProps(['propName'])
  </script>
  