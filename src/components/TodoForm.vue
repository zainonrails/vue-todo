<template>
  <div class="col-6 offset-3">
    <form>
      <div class="form-group">
        <label for="exampleInputEmail1" class="form-label">Add a Todo</label>
        <input v-model="todoContent" type="text" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
      </div>
      <button @click.prevent="onSubmit()" class="btn btn-primary">Add</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "TodoForm",
  data () {
    return {
      todoContent: ''
    }
  },
  methods: {
    onSubmit() {
      this.$emit('addTodo', { content: this.todoContent })
      this.todoContent = ''
    }
  }
}
</script>

<style scoped>

</style>