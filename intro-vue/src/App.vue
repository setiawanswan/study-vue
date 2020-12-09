<template>
<div id="app">
  <Todos  v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
</div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Todos from './components/Todos.vue'

export default{
  name: 'app',
  components: {
    Todos
  },
  data(){
    return {
      todos: [
        {
        "userId": 1,
        "id": 1,
        "title": "Todo One",
        "completed": true
        },
        {
        "userId": 1,
        "id": 2,
        "title": "Todo Two",
        "completed": false
        },
        {
        "userId": 1,
        "id": 3,
        "title": "Todo Three",
        "completed": false
        },
      ]
    }
  },
  methods: {
    deleteTodo(id){
      this.todos = this.todos.filter(todo => todo.id !== id)
    }
  }
}

</script>

