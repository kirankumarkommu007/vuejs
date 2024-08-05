<template>
    <div class="container">
      <h1>Saas Example Form</h1>
      <form @submit.prevent="submitForm">
        <div class="form-group">
          <label for="name">Name:</label>
          <input type="text" id="name" v-model="name" required />
        </div>
        <div class="form-group">
          <label for="feedback">Feedback:</label>
          <textarea id="feedback" v-model="feedback" required></textarea>
        </div>
        <button type="submit" class="button">Submit Feedback</button>
      </form>
      <div v-if="message" :class="['message', messageType]">{{ message }}</div>
    </div>
  </template>
  <script>
  export default {
    name: 'SaasComp',
    data() {
      return {
        name: '',
        feedback: '',
        message: '',
        messageType: ''
      };
    },
    methods: {
      submitForm() {
        if (this.name && this.feedback) {
          this.message = 'Thank you for your feedback!';
          this.messageType = 'success';
        } else {
          this.message = 'Please fill out all fields.';
          this.messageType = 'error';
        }
      }
    }
  }
  </script>
  
  <style lang="scss">
  $primary-color: #3498db;
  $secondary-color: #2ecc71;
  $font-stack: Helvetica, sans-serif;
  
  body {
    font-family: $font-stack;
    background-color: $secondary-color;
    margin: 0;
    padding: 20px;
  }
  
  .container {
    max-width: 600px;
    margin: auto;
    background: white;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
  
  .form-group {
    margin-bottom: 15px;
  
    label {
      display: block;
      margin-bottom: 5px;
    }
  
    input, textarea {
      width: 100%;
      padding: 10px;
      border: 1px solid #ccc;
      border-radius: 4px;
    }
  }
  
  .message {
    margin-top: 20px;
    padding: 10px;
    border-radius: 4px;
    font-size: 16px;
  
    &.success {
      border: 1px solid green;
      color: green;
      background-color: #e9f9e9;
    }
  
    &.error {
      border: 1px solid red;
      color: red;
      background-color: #f9e9e9;
    }
  }
  
  .button {
    background-color: $primary-color;
    border: none;
    color: white;
    padding: 10px 20px;
    font-size: 16px;
    margin-top: 10px;
    cursor: pointer;
  
    &:hover {
      background-color: darken($primary-color, 10%);
    }
  }
  </style>