<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Hello students
      <a href="https://cli.vuejs.org" target="_blank" rel="noopener"
        >vue-cli documentation</a
      >
    </p>

    <!-- Double mustache are used to be parse in javascript in vue -->
    <!-- Single mustache are used to be parse in html in vue -->

    {{ greeting }}

    
    <!-- v-model are used for two way data binding -->
    <!-- <input v-model="greeting" /> -->
    <input @keyup.enter="greet" v-model="greeting" />
    <hr />

    <!-- Like an if statement in js . If the div is truthy it will be rendered on the page but if it is falsy it will not be rendered on the page -->
    <div v-if="isVisible" class="box"></div>

    <!-- v-show is used to show and hide elements on the page -->
    <!-- it is almost the same as v-if but the only the difference is that the when the div is false the style is rendered as display:none;
    That means that the div is in the dom  but it is just not visible. -->
    <!-- It is used in  most cases when you want to toggle something on or off like harmburger and close icons. -->

    <div v-if="isVisible" class="box"></div>
    <!-- <div v-else-if="isVisible2" class="box-two"></div>
    <div v-else class="box-three"></div> -->

    <!-- The v-else-if works like the if else statement in js -->

    <!-- v-on is used specifically for events such as custom-events or browser event-->
    <!-- v-on:click is used to listen for click events -->
    <!-- v-on:click="incrementCount" is used to call a method when the click event is triggered -->
    <!-- To to create a toggle button you use the not operation -->
    <!-- Shorthand for v-on:click is @click -->
    <!-- Shorthand for key press events is @keyup or @keydown -->


    <!-- <button v-on:click="isVisible = !isVisible">Toggle Button</button> -->
    <button @click="toggleBox" >Toggle Box</button>
    <button v-on:click="isVisible = true">Show box</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },

  data() {
    return {
      isAvailable: false,
      count: 5,
      greeting: "Hello Vue 3!",
      isVisible: false,
      isVisible2: false,
    };
  },

  // methods are used to call functions in vue
  // methods are called in the template using v-on:click="incrementCount"
  //methods are object of functions.You can put as many function as possible in the method objects to be able to use it on my vue js application
  // Vue is responsible for putting all the variables in the this context so that it can be accessible anywhere in the vue application
  
  
  // event modifiers are used to listen for specific events such as keyup.enter or keyup.space
  //@click.prevent is used to prevent the default behaviour of the click event
  // @click.stop is used to stop the propagation of the click event
  // @click.self is used to listen for click events on the element itself and not on the child elements
  // @click.once is used to listen for click events only once
  // @click.right is used to listen for right click events
  // @click.middle is used to listen for middle click events
  // @click.left is used to listen for left click events
  // @click.ctrl is used to listen for click events when the ctrl key is pressed
  // @click.shift is used to listen for click events when the shift key is pressed
  // @click.alt is used to listen for click events when the alt key is pressed
  // @click.enter is used to listen for click events when the enter key is pressed
  // @click.esc is used to listen for click events when the esc key is pressed
  // @click.tab is used to listen for click events when the tab key is pressed
  // @click.delete is used to listen for click events when the delete key is pressed
  // @click.backspace is used to listen for click events when the backspace key is pressed
  // @click.up is used to listen for click events when the up key is pressed
  // @click.down is used to listen for click events when the down key is pressed
  // @click.space is used to listen for click events when the space key is pressed


  methods: {
    // incrementCount() {
    //   this.count++;
    // },
    toggleBox(){
      this.isVisible= !this.isVisible
    },
    greet(){
      console.log(this.greeting);
    }

  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.box {
  background-color: purple;
  height: 200px;
  width: 200px;
}
.box-two {
  background-color:blue;
  height: 200px;
  width: 200px;
}
.box-three {
  background-color: black;
  height: 200px;
  width: 200px;
}
</style>
