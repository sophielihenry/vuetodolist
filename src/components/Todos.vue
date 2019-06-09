<template>
  <div>
    <h1>Daily todos</h1>
    <div v-for="todo in todolist">
        <h3> {{todo.title}}</h3>

    </div>
  </div>



</template>

<script>
  export default {
    name: "Todos",
    props: ["todolist"]


  }




</script>

<style scoped>


</style>
