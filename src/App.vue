<template>
  <div id="app">
   <Teste/>
    <img src="./assets/chaton.jpg">
<!--    <HelloWorld/> -->
<Promotion v-for="name in names" v-bind:name="name"></Promotion>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld'
import Teste from './components/Teste';
import Promotion from './components/Promotion';

export default {
  name: 'App',
  components: {
   // HelloWorld,
    Teste,
    Promotion
  },
  data () {
    return {
      names: ["Aaron Swartz","Jimmy Wales","John Perry Barlow","Margaret hamilton"]
    }
  }
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
