<template>
    <div id="app">
      <div class="container">
        <h1>To Do List Vue</h1>
        <input type="text" v-model="newToDo">
        <button class="add-button">Add</button>
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
  }
}
</script>

<style>

</style>
