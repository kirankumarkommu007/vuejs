<template>
  <div>
    <h1>Fetched Data</h1>
    <button @click="fetchData" v-show="items.length === 0">Fetch Data</button>
    <button @click="refresh" v-show="items.length != 0">reset page</button>

    <ul>
      <li v-for="item in items" :key="item.id">{{ item.title }}</li>
    </ul>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'FetchDataComponent',
  data() {
    return {
      items: [],
      
    };
  },
  methods: {
    fetchData() {
      this.loading = true;
      axios.get('https://jsonplaceholder.typicode.com/posts')
    .then(response => {
      this.items = response.data;
    })
    .catch(error => {
      console.error('There was an error fetching the data:', error);
      // Optionally, you could set an error state here if you want to display an error message
    });
    },
    refresh(){
     this.items = []
    }
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
