<template>
<div id="app">
  <div>
    <input type="number" v-model="age">
    <div v-if="age < 18">
      Usia anda dibawah umur 18 tahun    
    </div>
    <div v-else-if="age > 25">
      Anda sudah terlalu tua
    </div>
    <div v-else>
      Usia anda mencukupi
    </div>
  </div>
  <div>
    <Todos  v-bind:todos="todos"/>
  </div>
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
      age: 21,
      todos: [
        {
        "userId": 1,
        "id": 1,
        "title": "Todo One",
        "completed": false
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
  }
}

</script>

