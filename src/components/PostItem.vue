<template>
  <div class="card">
    <div class="card-image">
      <img src="https://via.placeholder.com/900x600/333/fff" alt />
    </div>
    <div class="card-content">
      <h4 class="title is-6 mb-2">{{post.title}}</h4>
      <p class="mb-3 has-text-dark">{{post.body}}</p>
      <a href="#" class="button is-primary">read more</a>
    </div>
  </div>
</template>

<script>
export default {
  name: "PostItem",
  props: ["post"],
};
</script>

