<template>
  <div class="NeuCard">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "NeuCard",
  props: {}
};
</script>

<style scoped>
.NeuCard {
  width: 300px;
  height: 400px;
}
.NeuCard {
  color: #868a9a;
  padding: 16px;
  background-color: #ebecf0;
  text-shadow: 1px 1px 0 #fff;
  font-size: 16px;
  border-radius: 50px;
  width: 100%;
  border: none;
  outline: none;
  cursor: pointer;
  box-shadow: 2px 2px 5px #babecc, -2px -2px 5px #fff;
}
</style>
