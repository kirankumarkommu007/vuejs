<template>
    <div>
      <h1>Fetched Data</h1>
      <button @click="fetchData">Fetch Data</button>
      <ul>
        <li v-for="item in items" :key="item.id">{{ item.title }}</li>
      </ul>
      <div v-if="loading">Loading...</div>
    </div>
  </template>
  
  <script>
  import axios from 'axios';
  
  export default {
    name: 'FetchDataComponent',
    data() {
      return {
        items: [],
        loading: false,
      };
    },
    methods: {
      fetchData() {
        this.loading = true;
  
        axios.get('https://jsonplaceholder.typicode.com/posts')
          .then(response => {
            this.items = response.data;
          })
          .finally(() => {
            this.loading = false;
          });
      },
    },
  };
  </script>
  
  <style>
  h1 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  
  button {
    margin-bottom: 10px;
    padding: 10px 20px;
    font-size: 16px;
    cursor: pointer;
    background-color: #4CAF50;
    color: white;
    border: none;
    border-radius: 4px;
  }
  
  button:hover {
    background-color: #45a049;
  }
  
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    background: #f9f9f9;
    margin: 5px 0;
    padding: 10px;
    border: 1px solid #ddd;
  }
  </style>
  