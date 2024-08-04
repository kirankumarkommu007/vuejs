<!-- src/components/SimpleCounter.vue -->
<template>
  <button @click="increment">Clicks: {{ count }}</button>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'SimpleCounterComposition',
  setup() {
    const count = ref(0);
    
    function increment() {
      count.value++;
    }
    
    return {
      count,
      increment
    };
  }
};
</script>

<style>
button {
  background: gainsboro;
}
</style>
