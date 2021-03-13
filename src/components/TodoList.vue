<template>
  <div>
    <input v-model="newTodo" type="text" class="todo-input" placeholder="What needs to be done">
    <div v-for="todo in todos" :key="todo.id" class="todo-item">
      {{todo.title}}
    </div>
  </div>
</template>

<script>
export default {
  name: 'todo-list',
  data(){
    return{
      newTodo: '',
      todos:[
        {
          'id': 1,
          'title': 'Finish',
          'completed':false,
        },
         {
          'id': 2,
          'title': 'Take over',
          'completed':false,
        },
      ]
    }
  }
}
</script>
<style lang="scss">
  .todo-input {
    width: 100%;
    padding: 10px 18px;
    font-size: 18px;
    margin-bottom: 16px;

    &:focus{
      outline:0px;
    }
  }
</style>