<template>
    <div>
      <p>Count: {{ count }}</p>
      <p>Double Count: {{ doubleCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </template>
  
  <script>
  import { ref, computed, watch, defineComponent } from 'vue';
  
  export default defineComponent({
    name: 'CounterCompositionAPI',
    props: {
      initialCount: {
        type: Number,
        default: 0
      }
    },
    setup(props, { emit }) {
      const count = ref(props.initialCount);
  
      const increment = () => {
        count.value++;
        emit('count-changed', count.value);
      };
  
      const doubleCount = computed(() => count.value * 2);
  
      watch(count, (newVal) => {
        console.log('Count changed to:', newVal);
      });
  
      return {
        count,
        increment,
        doubleCount
      };
    }
  });
  </script>
  
  <style>
  button {
    background-color: lightcoral;
    padding: 10px;
  }
  </style>
  