<template>
  <div class="box" v-bind:class="{'has-background-warning':todo.completed}">
    <span class="tag is-dark">#{{index+1}}</span>
    {{todo.title}}
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo", "index"]
};
</script>