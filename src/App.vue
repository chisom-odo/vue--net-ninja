<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Your Vue.js App"/>
  <AltschoolStudent />
  <NameOfMySchool />
  <LoginForm />
  <CustomInput />
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AltschoolStudent from './components/AltschoolStudent.vue';
import NameOfMySchool from './components/NameOfMySchool.vue'
import LoginForm from './components/LoginForm.vue'
import CustomInput from './components/CustomInput.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    AltschoolStudent,
    NameOfMySchool,
    LoginForm,
    CustomInput,
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
