<template>
  <div class="container">
    <img alt="Vue logo" class="logo" src="../assets/logo.png">
    <TodoList></TodoList>
  </div>
</template>

<script>
// @ is an alias to /src
import TodoList from '../components/TodoList.vue'

export default {
  name: 'Home',
  components: {
    TodoList
  }
}
</script>

<style lang="scss">
*{
  box-sizing: border-box;
}
.container{
  max-width: 600px;
  margin: 0 auto;
}
.logo{
  display: block;
  margin: 20px auto;
  height: 75px;
}
</style>
