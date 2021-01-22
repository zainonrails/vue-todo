<template>
  <li class="list-group-item"> {{content}}
    <button @click.prevent="deleteTodo(index)" type="button" class="close" aria-label="Close">
      <span aria-hidden="true">&times;</span>
    </button>
  </li>
</template>

<script>
export default {
  name: "TodoItem",
  props: ['content', 'index'],
  methods: {
    deleteTodo(index) {
      this.$emit('deleteTodo', index)
    }
  }
}
</script>

<style scoped>

</style>