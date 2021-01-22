<template>
  <div>
    <img width="250" class="img-fluid " alt="Vue logo" src="./assets/todologo.png">
  </div>
  <ListContainer/>
</template>

<script>
import ListContainer from './components/ListContainer';

export default {
  name: 'App',
  components: {
    ListContainer
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
