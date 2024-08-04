<template>
  <div>
  <SimpleCounter />
  <br>
<ClickCounter />
<br>
<HoverCounter />  
</div>
</template>

<script>
import ClickCounter from './components/ClickCounter.vue';
import HoverCounter from './components/HoverCounter.vue'
import SimpleCounter from './components/SimpleCounter.vue';
export default {
  name: 'App',
  components: {
    ClickCounter,
    HoverCounter,
    SimpleCounter
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
