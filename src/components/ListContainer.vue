<template>
  <div>
    <TodoForm @add-todo="added($event)"></TodoForm>
    <TodoList :todos="todos"></TodoList>
  </div>
</template>

<script>
import TodoList from './TodoList';
import TodoForm from './TodoForm';

export default {
  name: "ListContainer",
  components: {
    TodoList,
    TodoForm
  },
  data() {
    return {
      todos: []
    }
  },
  methods: {
    added(todo) {
      this.todos.push(todo.content)
      console.log(this.todos)
    }
  }
}
</script>

<style scoped>

</style>