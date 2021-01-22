<template>
  <div class="col-6 offset-3 mb-5">
    <div class="mt-5">
      <p>TodoList</p>
      <ul class="list-group" :key="index" v-for="(todo, index) in myTodos">
        <TodoItem
        :content="todo"
        :index="index"
        @deleteTodo="deleteTodo"
        />
<!--        <li class="list-group-item"> {{todo}}-->
<!--          <button @click.prevent="deleteTodo(index)" type="button" class="close" aria-label="Close">-->
<!--            <span aria-hidden="true">&times;</span>-->
<!--          </button>-->
<!--        </li>-->
      </ul>
    </div>
  </div>
</template>

<script>
import TodoItem from '@/components/TodoItem.vue';

export default {
  name: "TodoList",
  components: {
    TodoItem
  },
  props: ['todos'],
  data() {
    return {
      myTodos: this.todos
    }
  },
  methods: {
    deleteTodo(index) {
      console.log('removed from ' + index)
      this.myTodos.splice(index, 1)
    }
  }
}
</script>

<style scoped>

</style>