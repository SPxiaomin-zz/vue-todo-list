<template>
  <div class="todo-input">
    <input
      type="text"
      v-model="newTodoText"
      @keyup.enter="addNewTodo"
    >
  </div>
</template>

<script>
export default {
  name: 'TodoInput',
  data () {
    return {
      newTodoText: '',
    }
  },
  methods: {
    addNewTodo () {
      this.$emit('newTodoTextComing', this.newTodoText)
      this.newTodoText = ''
    },
  },
  props: {

  }
}
</script>
