<template>
    <div>
      <h1>Lifecycle Hooks Example</h1>
      <p>{{ message }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'LifecycleHooks',
    data() {
      return {
        message: 'hi, Vue!',
      };
    },
    beforeCreate() {
      console.log('beforeCreate: Component instance is being created.');
    },
    created() {
      console.log('created: Component instance has been created.');
    },
    beforeMount() {
      console.log('beforeMount: Component is about to be mounted.');
    },
    mounted() {
      console.log('mounted: Component has been mounted.');
    },
    beforeUpdate() {
      console.log('beforeUpdate: Data is about to be updated.');
    },
    updated() {
      console.log('updated: Data has been updated.');
    },
    beforeUnmounted() {
      console.log('beforeDestroy: Component is about to be destroyed.');
    },
    unmounted() {
      console.log('destroyed: Component has been destroyed.');
    },
    methods: {
      updateMessage() {
        this.message = 'Updated message!';
      }
    }
  };
  </script>
  
  <style>
  h1 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  </style>
  