<template>
  <div id="app">
    <NavBar/>
   
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
       <router-link to="/blogs">Blogs</router-link> 
      <router-view/>

<p>{{ 2+2 }}</p>

 <p> {{message}}</p>
 <p> {{message2}}</p>
<button @click ="convertMessage()">Click for Uppercase</button>

       <Footer/>
  </div>
</template>

<script>

import NavBar from './components/NavBar.vue'
import Footer from './components/Footer.vue'

export default {
components: {
  NavBar,
  Footer,
},
data(){
  return{
    message: "This is a text",
    message2: ""
  };
},

methods: {
 
 convertMessage(){
    this.message2 = this.message.toUpperCase(); 
 },
},

}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}
</style>
