<template>
    <div>
      <p>Count: {{ count }}</p>
      <p>Double Count: {{ doubleCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref, computed } from 'vue';
  
  export default {
    name: 'CounterCompositionAPI',
    setup() {
      const count = ref(0);
  
      const increment = () => {
        count.value++;
        console.log(count)
        console.log(count.value)

      };
  
      const doubleCount = computed(() => count.value * 2);
  
      return {
        count,
        increment,
        doubleCount
      };
    }
  };
  </script>
  
  <style>
  </style>
  