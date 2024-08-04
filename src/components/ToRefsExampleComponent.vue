<template>
    <div>
      <h1>ToRefs Example</h1>
      <p>Name: {{ name }}</p>
      <p>Age: {{ age }}</p>
      <button @click="increaseAge">Increase Age</button>
    </div>
  </template>
  
  <script>
  import { reactive, toRefs } from 'vue';
  
  export default {
    name: 'ToRefsExampleComponent',
    setup() {
      const person = reactive({
        name: 'Kiran Kumar',
        age: 25
      });
  
      function increaseAge() {
        person.age++;
        console.log(person)
        console.log(person.value)
        console.log(person.age)
        console.log(person.name)
      }
  
      const { name, age } = toRefs(person);
  
      return {
        name,
        age,
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
  