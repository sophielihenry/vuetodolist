<template>
  <div id="app">
    <AddTodo v-on:add-todo="addTodo" />
    <Todos v-bind:todolist="todolist" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
  import Todos from "./components/Todos.vue"
  import AddTodo from "./components/AddTodo.vue"

export default {
  name: 'app',
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todolist: [
        {
          id : 1,
          title: "wash dishes",
          completed: false
        },
        {
          id : 2,
          title: "clean room",
          completed: false
       }
      ],
    }
  },
    methods: {
        deleteTodo(id) {
          this.todolist = this.todolist.filter( todo => todo.id !== id )
        },
        addTodo(newTodo) {
          this.todolist = [...this.todolist, newTodo]
        }
      }
}
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
