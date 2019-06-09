<template>
  <div>
    <h1>Daily todos</h1>
    <div v-bind:key="todo.id" v-for="todo in todolist">
        <TodoItem v-bind:todo="todo" v-on:delete-todo="$emit('delete-todo', todo.id)"/>

    </div>
  </div>



</template>

<script>
   import TodoItem from  "./TodoItem.vue"


  export default {
    name: "Todos",
    components: {
      TodoItem
    },
    props: ["todolist"]
  }




</script>

<style scoped>


</style>
