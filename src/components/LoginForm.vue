<template>
    <form @submit.prevent="handleSubmit">
      <h1>{{ title }}</h1>
      <input type="email" placeholder="Email" v-model="email" />
      <input type="password" placeholder="Password" v-model="password"/>
      <button>Login</button>
    </form>
  </template>
  
  <script>
  
  export default {
    name: "LoginForm",
    data() {
      return {
        title: "Login Form",
        email: "",
        password: "",
      };
    },
    methods: {
      handleSubmit() {
        console.log("submitted");
          console.log(this.email, this.password);
  
      },
    },
  };
  </script>
  
  <style scoped>
  form {
    display: flex;
    flex-direction: column;
    gap:16px;
    width: 300px;
    margin: 0 auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  </style>
  