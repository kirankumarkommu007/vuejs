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
    props: {
      initialCount: {
        type: Number,
        default: 0
      }
    },
    data() {
      return {
        count: this.initialCount
      };
    },
    computed: {
      doubleCount() {
        return this.count * 2;
      }
    },
    methods: {
      increment() {
        this.count++;
        this.$emit('count-changed', this.count);
      }
    },
    watch: {
      count(newVal) {
        console.log('Count changed to:', newVal);
      }
    }
  };
  </script>
  
  <style>
  button {
    background-color: lightblue;
    padding: 10px;
  }
  </style>
  