<!-- src/components/HoverCounterComposition.vue -->
<template>
  <button @mouseover="increment">Hovers: {{ count }}</button>
</template>

<script>
import { useCounter } from './composables/useCounter';

export default {
  name: 'HoverCounterComposition',
  setup() {
    const { count, increment } = useCounter();
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
