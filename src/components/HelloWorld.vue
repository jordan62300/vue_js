<template>
  <img src="assets/chaton.jpg"
  <div class="hello">
    <h1>{{ msg }}</h1>
    <h2 class="purple">{{ messagedeux }}</h2>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Hello world',
      messagedeux: 'Coucou Gwenaelle'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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

.purple {
  color: purple;
}
</style>
