<template>
    <div>
      <p>Count: {{ count }}</p>
      <p>Double Count: {{ doubleCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'CounterOptionsAPI',
    data() {
      return {
        count: 0
      };
    },
    methods: {
      increment() {
        this.count++;
        console.log(this.count)
      }
    },
    computed: {
      doubleCount() {
        
        return this.count * 2;

      }
    }
  };
  </script>
  
  <style>
  </style>
  