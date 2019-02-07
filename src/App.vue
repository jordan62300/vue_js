<template>
  <div id="app">
   <Teste/>
    <img src="./assets/chaton.jpg">
<!--    <HelloWorld/> -->
<Promotion v-for="promotion in promotions" v-bind:key="promotion.id" v-bind:name="promotion.name"></Promotion>
<!--<Promotion v-for="name in names" v-bind:key="name" v-bind:name="name"></Promotion> -->
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
      names: ["Aaron Swartz","Jimmy Wales","John Perry Barlow","Margaret hamilton"],
      promotions: []
    }
  },
  methods: {
    getPromotions: function() {
      fetch("http://api-students.popschool-lens.fr/api/promotions")
      .then(r => r.json())
      .then(r => function () {
        console.log("ok")
        this.promotion = r["hydra:member"]
      })
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
