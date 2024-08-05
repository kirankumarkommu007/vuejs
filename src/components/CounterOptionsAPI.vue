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
  emits: ['update:count'],
  data() {
    return {
      count: this.initialCount
    };
  },
  methods: {
    increment() {
      this.count++;
      this.$emit('update:count', this.count);
    }
  },
  computed: {
    doubleCount() {
      return this.count * 2;
    }
  },
  watch: {
    count(newValue, oldValue) {
      console.log(`Count changed from ${oldValue} to ${newValue}`);
    }
  }
};
</script>

<style>
</style>
