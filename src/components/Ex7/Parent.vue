<template>
    <div>
        <h1>Bài 7</h1>
        <ChildrenComponent ref="childComponentRef"/>
      <button @click="accessChildComponent">Send Message</button>
    </div>
  </template>
  
  <script>
  import ChildrenComponent from './Child.vue'
  
  export default {
    components: {
    ChildrenComponent
  },
    methods: {
      accessChildComponent() {
        this.$refs.childComponentRef.childMethod();
      }
    }
  }
  </script>
  