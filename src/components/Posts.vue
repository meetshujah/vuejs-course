<template>
  <div class="columns is-multiline">
    <div class="column is-3" v-for="post in posts" v-bind:key="post.id">
      <PostItem :post="post" />
    </div>
  </div>
</template>

<script>
import PostItem from "./PostItem";
export default {
  components: {
    PostItem,
  },
  name: "Posts",
  props: ["posts"],
};
</script>