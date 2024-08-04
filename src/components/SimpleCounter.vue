<!-- src/components/ClickCounter.vue -->
<template>
    <button @click="increment">Clicks: {{ count }}</button>
  </template>
  
  <script>
  
  export default {
    name:'SimpleCounter',
    data(){
        return {
            count : 0
        }
    },
    methods:{
        increment(){
            this.count +=1
        }
    }
  };
  </script>

<style >
  button {
    background: gainsboro;
  }
  </style>
  