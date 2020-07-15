<template>
  <div class="box" v-bind:style="{'background-color': color}" @click="$emit('changeColor',color)"></div>
</template>

<script>
export default {
  name: "ColorBox",
  props: ["color"]
};
</script>

<style scoped>
.box:hover {
  cursor: pointer;
  opacity: 0.6;
}
</style>