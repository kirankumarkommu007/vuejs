<template>
 <RefExampleComponent />
 <ReactiveExampleComponent />
 <ToRefsExampleComponent />
</template>

<script>
import RefExampleComponent from './components/RefExampleComponent.vue';
import ReactiveExampleComponent from './components/ReactiveExampleComponent.vue';
import ToRefsExampleComponent from './components/ToRefsExampleComponent.vue';

export default {
  name: 'App',
  components: {
    RefExampleComponent,
    ReactiveExampleComponent,
    ToRefsExampleComponent,
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
