<template>
    <div>
      <h1>Ref Example</h1>
      <p>Count: {{ count }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref } from 'vue';
  
  export default {
    name: 'RefExampleComponent',
    setup() {
      const count = ref(0);
  
      function increment() {
        count.value++;
        console.log(count)
        console.log(count.value)
      }
  
      return {
        count,
        increment
      };
    }
  };
  </script>
  
  <style>
  h1 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  button {
    padding: 10px 20px;
    font-size: 16px;
  }
  </style>
  