<template>
    <div class="studentItem">
    <h1> {{ me.firstname + " " +me.lastname}} </h1>
    <div> {{myURL}} </div>
    </div>
</template>

<script>

export default {
  name: 'Student',
  data() {
      return {
      me: {},
      }
  },
  props: {
      myURL: String,
  },
  methods: {
      getMe: function () {
          fetch("http://api-students.popschool-lens.fr" + this.myURL)
          .then(r => r.json())
          .then(r => {
              console.log(r)
              this.me = r;
          })
      }

      },
  
  mounted () {
      this.getMe()
  }
}

</script>

<style scoped>
.studentItem{
    display: block;
    border: 1px solid black;
    background-color: #1da1f2; 
    padding : 6px;
}
</style>