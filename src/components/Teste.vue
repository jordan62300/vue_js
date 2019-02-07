<template>
    <div class="container">
        <div class="row">
        <h1>Gestion de promotion</h1>
            <h2 class="purple">{{firstmessage}}</h2>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Hello world',
      firstmessage: 'Coucou Gwenaelle'
    }
  }
}
</script>

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
