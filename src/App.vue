<template>
  <div>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Satyam Mishra"/>
  <Home/>
  <About/>
  <Child name="html-binding"/>
  <simpleform/>
  </div>
</template>

<script>

import Home from './components/Home.vue'
import About from './components/About.vue'
import Child from './components/Child.vue'
import simpleform from './components/simpleform.vue'

export default {
  name: 'App',
  components: {
    Home,
    About,
    Child,
    simpleform
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
