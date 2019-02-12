<template>
    <div class="promotion">
        <h1>{{ promotion.name }}</h1>
        <input type="text" v-model="promotion.name">
       <div> {{ promotion.id }}
         - Début: {{ promotion.startDate }}
          - Fin: {{ promotion.endDate }}</div> 
    </div>
</template>

<script>
export default {
  name: 'Promotion',
  props: {
      promotion: Object,
    },
    methods: {
        update(event) {
            console.log(event.target.value);
        }
    }
  };

</script>

<style scoped>
.promotion {
    margin: 10px;
    background-color: red;
    border: solid 1px black;
}
</style>
