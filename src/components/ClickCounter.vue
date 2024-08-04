<!-- src/components/ClickCounter.vue -->
<template>
    <button @click="increment">Clicks: {{ count }}</button>
  </template>
  
  <script>
  import counterMixin from '@/mixins/counterMixin';
  
  export default {
    name:'ClickCounter',
    mixins: [counterMixin]
  };
  </script>
  <style >
  button {
    background: gainsboro;
  }
  </style>