<template>
  <div>
    <p>Count: {{ count }}</p>
    <p>Double Count: {{ doubleCount }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script>
import { ref, computed, watch } from 'vue';

export default {
  name: 'CounterCompositionAPI',
  props: {
    initialCount: {
      type: Number,
      default: 0
    }
  },
  emits: ['update:count'],
  setup(props, { emit }) {
    const count = ref(props.initialCount);

    const increment = () => {
      count.value++;
      emit('update:count', count.value);
    };

    const doubleCount = computed(() => count.value * 2);

    watch(count, (newValue, oldValue) => {
      console.log(`Count changed from ${oldValue} to ${newValue}`);
    });

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
