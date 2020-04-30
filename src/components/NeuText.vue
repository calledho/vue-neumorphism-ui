<template>
  <div class="headline">
    <h1><slot></slot></h1>
  </div>
</template>

<script>
export default {
  name: "NeuInput",
  props: {}
};
</script>

<style scoped>
.headline {
  color: #868a9a;
  text-shadow: 1px 1px 1px #fff;
  text-align: center;
  text-transform: uppercase;
}
</style>
