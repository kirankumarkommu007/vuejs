<!-- src/components/ClickCounter.vue -->
<template>
  <button class="button" @click="increment">Clicks: {{ count }}</button>
</template>

<script>
import { useCounter } from './composables/useCounter';

export default {
  name: 'ClickCounterComposition',
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
  background:green;
  border-style: none;
}
</style>
