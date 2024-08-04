<template>
    <div>
      <h1>Reactive Example</h1>
      <p>Name: {{ person.name }}</p>
      <p>Age: {{ person.age }}</p>
      <button @click="increaseAge">Increase Age</button>
    </div>
  </template>
  
  <script>
  import { reactive } from 'vue';
  
  export default {
    name: 'ReactiveExampleComponent',
    setup() {
      const person = reactive({
        name: 'Shiva Pabbu',
        age: 30
      });
  
      function increaseAge() {
        person.age++;
        console.log(person)
        console.log(person.value)
        console.log(person.age)
        console.log(person.name)

      }
  
      return {
        person,
        increaseAge
      };
    }
  };
  </script>
  
  <style>
  h1 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  button {
    padding: 10px 20px;
    font-size: 16px;
  }
  </style>
  