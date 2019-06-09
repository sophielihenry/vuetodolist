<template>
  <div class="todoItemStyle" v-bind:class="{ 'is-complete': todo.completed }">
    <input type="checkbox" v-on:change="markComplete">
      <p>{{ todo.title }}</p>
    <button class="delete" @click="$emit('delete-todo', todo.id)">x</button>
  </div>
</template>

<script>
  export default {
    name: "TodoItem",
    props: ["todo"],
    methods: {
      markComplete() {
        this.todo.completed = !this.todo.completed
      }
    }
}
</script>

<style scoped>
  .is-complete {
    text-decoration: line-through;
  }

  .todoItemStyle {
    display: flex;
    justify-content: space-around;
    width: 25vw;
    margin: auto;
    align-items: center;
  }

</style>
