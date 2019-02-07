<template>
    <div class="promotion">
        <h1>{{ name }}</h1>
    </div>
</template>

<script>
export default {
  name: 'Promotion',
  props: {
      name: String
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
