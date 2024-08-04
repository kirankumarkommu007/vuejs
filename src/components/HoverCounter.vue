<!-- src/components/HoverCounter.vue -->
<template>
    <div @mouseover="increment">Hovers: {{ count }}</div>
  </template>
  
  <script>
  import counterMixin from '@/mixins/counterMixin';
  
  export default {
    name:'HoverCounter',
    mixins: [counterMixin]
  };
  </script>
  
  <style >
  div {
    background: gainsboro;
  }
  </style>
  