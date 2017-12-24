<template>
  <div class="todo-list">
    <ul>
      <TodoListItem
        v-for="(todo, index) in todos"
        :key="index"
        :todo="todo"
      >
      </TodoListItem>
    </ul>
  </div>
</template>

<script>
import TodoListItem from './TodoListItem'

export default {
  name: 'TodoList',
  components: {
    TodoListItem,
  },
  props: {
    todos: {
      type: Array,
      required: true,
    },
  },
}
</script>
