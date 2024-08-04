<template>
  <div>
  <SimpleCounterComposition />
  <br>
<ClickCounterComposition />
<br>
<HoverCounterComposition />  
</div>
</template>

<script>
import ClickCounterComposition from './components/ClickCounterComposition.vue';
import HoverCounterComposition from './components/HoverCounterComposition.vue'
import SimpleCounterComposition from './components/SimpleCounterComposition.vue';
export default {
  name: 'App',
  components: {
    ClickCounterComposition,
    HoverCounterComposition,
    SimpleCounterComposition
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
