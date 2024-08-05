<template>
  <div id="app">
    <h1>Options API Component</h1>
    <CounterOptionsAPI :initialCount="5" @count-changed="handleCountChange" />

    <h1>Composition API Component</h1>
    <CounterCompositionAPI :initialCount="10" @count-changed="handleCountChange" />
  </div>
</template>


<script>
import CounterCompositionAPI from './components/CounterCompositionAPI.vue';
import CounterOptionsAPI from './components/CounterOptionsAPI.vue';


export default {
  name: 'App',
  components: {
    CounterCompositionAPI,
    CounterOptionsAPI
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
