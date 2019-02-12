<template>
    <div class="promotion">
        <h1>{{ promotion.name }}</h1>
        <input type="text" v-model="promotion.name">
       <div> {{ promotion.id }}
         - Début: {{ promotion.startDate }}
          - Fin: {{ promotion.endDate }}</div> 
          <Student  v-for="(studentURL,index) in promotion.students" v-bin:key="index" v-bind:myURL="studentURL"></Student>
       <!--   <ul class="studentList">
            <li v-for="studentURL in promotion.students" class="studentItem">{{ studentURL }}</li>
          </ul> -->
    </div>
</template>

<script>

import Student from './Student'

export default {
  name: 'Promotion',
  props: {
      promotion: Object,
    },
    components: {
        Student,
    },
    methods: {
        update(event) {
            console.log(promotion.name + "updated");
        },
        delete(event) {
            console.log(promotion.name + "deleted")
        }
    }
  };

</script>

<style scoped>
.promotion {
    margin: 10px;
    background-color: red;
    border: solid 1px black;
    border-radius: 30px;
}

.studentList{
    display:flex;
    border:2px dotted red;
    border-radius:30px;
    margin:5px 50px;
    background-color:grey;
}

.studentItem{
    display: block;
    border: 1px solid black;
    background-color: #1da1f2; 
    padding : 6px;
}
</style>
