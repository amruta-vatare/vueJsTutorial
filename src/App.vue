<template>
   <MyPractice myprop="My first component property"></MyPractice>
    <hr/>
    <Exercise1/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <Exercise2Vue/>
    <Exercise3Vue></Exercise3Vue>
   <hr/>
 
</template>

<script>
import Exercise1 from './components/Exercise1.vue';
import HelloWorld from './components/HelloWorld.vue'
import MyPractice from './components/MyPractice.vue'
import Exercise2Vue from './components/Exercise2.vue';
import Exercise3Vue from './components/Exercise3.vue';
export default {
  name: 'App',
  components: {
    HelloWorld,
    MyPractice,
    Exercise1,
    Exercise2Vue,
    Exercise3Vue
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
