<template>
    <div class="todo-item">
        <div class="todo-item-left">
            <input type="checkbox" v-model="completed"/>
            <div class="todo-item-label" :class="{ completed : completed }" v-if="!todo.editing" @dblclick="editTodo">{{ title }}</div>
            <input class="todo-item-edit" type="text" v-model="title" v-else v-focus @blur="doneEdit" @keyup.enter="doneEdit" @keyup.esc="cancelEdit" />
        </div>
        <div class="remove-item" @click="removeTodo(index)">&times;</div>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  name: 'Todo',
  data() {
      return {
          id: this.todo.id,
          title: this.todo.title,
          completed: this.todo.completed,
          editing: this.todo.editing,
          beforeEditCache: ''
      }
  },
  methods: {
      removeTodo(index: Number){
          this.$emit('removeTodo', index)
      }
  },
  props: {
    todo: {
        type: Object,
        required: true
    },
    index: {
        type: Number,
        required: true
    }
  },
});
</script>

<style scoped>

</style>
