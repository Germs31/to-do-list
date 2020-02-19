<template>
    <div >
      <AddTodo />
      <TodoList />
    </div>
</template>

<script>
import TodoList from './components/TodoList'
import AddTodo from './components/AddTodo'
export default {
  components : {
    TodoList,
    AddTodo
  },
  data() {
    return {
      todos: [
        {

        }
      ]
    }
  },
}
</script>

<style>

</style>
