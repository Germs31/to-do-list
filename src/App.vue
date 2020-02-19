<template>
    <div id="app">
      <div class="container">
        <h1>To Do List Vue</h1>
        <input type="text" v-model="newToDo">
        <button class="add-button" v-on:click="add()">Add</button>
        <ul>
          <li v-bind:key="todo.id" v-for="todo in existingToDo" >
            <span>
              {{todo.text}}
            </span> 
            <button class="delete" @click="deleteToDo()"> 
              X
            </button>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>

export default {
  name: 'app',
  data () {
    return {
      newToDo: '',
      existingToDo: [
        {text: 'get food', id: 0},
        {text: 'go to work', id: 1},
        {text: 'go to gym', id: 2},
      ]
    }
  },
  methods: {
    add() {
      this.existingToDo.push({
        text: this.newToDo,
        id: new Date().valueOf()
      }),
      this.newToDo =''
    },
    deleteToDo(i) {
      this.existingToDo.splice(i, 1)
    }
  }
  
}
</script>

<style>
*{
  margin: 0;
}

body{
  background: #379683;
  color: #edf5e1;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

input[type=text]{
  margin-top: 1rem;
  width: 100%;
}

.add-button{
  width: 100%;
}

ul{
  list-style: none;
  margin-top: 2rem;
  display: flex;
  flex-direction: column;
}

.container{
  background: #05386b;
  padding: 2rem;
}
</style>


