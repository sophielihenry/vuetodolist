<template>
  <div id="app">

  </div>
</template>

<script>

export default {
  name: 'app',
  components: {


  },
  data() {
    return {
      todoList: [
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
      ]
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
