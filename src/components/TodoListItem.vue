<template>
  <li class="todo-list-item" @click="toggleDone">
    <span
      v-text="todo.text"
      :class="{ done: todo.isDone }"
    >
    </span>
  </li>
</template>

<script>
export default {
  name: 'TodoListItem',
  methods: {
    toggleDone () {
      this.todo.isDone= !this.todo.isDone
    },
  },
  props: {
    todo: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style scoped>
.done {
  text-decoration: underline;
}
</style>
