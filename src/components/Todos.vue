<template>
  <div class="columns is-multiline">
    <div v-for="(todo,index) in todos" v-bind:key="todo.id" class="column is-12 mb-4">
      <TodoItem v-bind:todo="todo" v-bind:index="index" />
    </div>
  </div>
</template>

<script>
import TodoItem from "./TodoItem";
export default {
  name: "Todos",
  components: {
    TodoItem
  },
  props: ["todos"]
};
</script>