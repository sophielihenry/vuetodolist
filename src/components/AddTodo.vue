<template>
  <div>
    <form @submit="addTodo">
      <input type="text" v-model="title" placeholder="add in a todo" name="title">
      <input type="submit" value="submit">
    </form>
  </div>
</template>

<script>
  export default {
    name: "AddTodo",
    data() {
      return {
        title: ''
      }
    },
    methods: {
      addTodo(e) {
        e.preventDefault();
        const newTodo = {
          id: Date.now(),
          title: this.title,
          completed: false
        }

        this.$emit('add-todo', newTodo);
        this.title = " ";
      }
    }
  }
</script>


<style scoped>

</style>


