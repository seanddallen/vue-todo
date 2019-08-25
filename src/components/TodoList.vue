<template>

</template>

<script lang="ts">
import Vue from 'vue';
import Todo from './Todo.vue'

export default Vue.extend({
  name: 'TodoList',
  props: {
    msg: String,
  },
});
</script>

<style scoped>

</style>
