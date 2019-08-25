<template>
  <div id="app" class="container">
    <img alt="Vue logo" src="./assets/logo.png" class="logo">
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
import TodoList from './components/TodoList.vue'

export default Vue.extend({
  name: 'app',
  components: {
  },
});
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
