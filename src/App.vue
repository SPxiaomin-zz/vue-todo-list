<template>
  <div id="todo">
    <TodoInput v-on:newTodoTextComing="handleNewTodoText"></TodoInput>
    <TodoList :todos="todos"></TodoList>
  </div>
</template>

<script>
import TodoInput from './components/TodoInput'
import TodoList from './components/TodoList'

export default {
  name: 'app',
  data () {
    return {
      todos: [],
    }
  },
  methods: {
    handleNewTodoText (newTodoText) {
      this.todos.unshift({
        text: newTodoText,
        isDone: false,
      })
    },
  },
  components: {
    TodoInput,
    TodoList,
  },
}
</script>

<style>
</style>
