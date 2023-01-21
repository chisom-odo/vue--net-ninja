<template>
  <form @submit.prevent="handleSubmit">
    <h1>{{ title }}</h1>
    <CustomInput type="email" placeholder="Email" v-model="email" v-bind:label="emailLabel" />
    <CustomInput type="password" placeholder="Password" v-model="password" v-bind:label="passwordLabel"/>
    <button>Login</button>
  </form>
</template>

<!-- if you want to parse a  variable from parent to child components follow this steps:
-- Go to the parent components and insert the variables in the data object
-- Use v-bind attribute to bind a js as a variable attribute on the parent component -->



<script>
import CustomInput from '../components/CustomInput.vue'

export default {
  name: "LoginForm",
  data() {
    return {
      title: "Login Form",
      email: "",
      password: "",
      emailLabel:'Email',
      passwordLabel:'Password',

    };
  },
  components:{
    CustomInput,
  },

  methods: {
    handleSubmit() {
      console.log("submitted");
      console.log(this.email, this.password);
    },
  },
  
  }
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  gap: 16px;
  width: 300px;
  margin: 0 auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 5px;
}
</style>
