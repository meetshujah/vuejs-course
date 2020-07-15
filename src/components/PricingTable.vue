<template>
  <div class="box has-text-centered">
    <slot name="header" />
    <slot name="body" />
    <slot name="footer" />
  </div>
</template>

<script>
export default {
  name: "PricingTable"
};
</script>