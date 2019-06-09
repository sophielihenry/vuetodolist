<template>
  <div id="app">
    <Todos v-bind:todolist="todolist" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
  import Todos from "./components/Todos.vue"

export default {
  name: 'app',
  components: {
    Todos
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
