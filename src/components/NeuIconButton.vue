<template>
  <div class="NeuIconButton">
    <button :class="icon"></button>
  </div>
</template>

<script>
export default {
  name: "NeuIconButton",
  props: {
    icon: {
      type: String,
      default: ""
    }
  }
};
</script>

<style scoped>
button {
  color: hsl(228, 9%, 56%);
  padding: 16px;
  background-color: #ebecf0;
  text-shadow: 1px 1px 0 #fff;
  font-size: 20px;
  border-radius: 320px;
  width: 100%;
  border: none;
  outline: none;
  cursor: pointer;
  box-shadow: 4px 4px 18px #babecc, -5px -5px 10px #fff;
  transition: all 0.2s ease-in-out;
}
button:hover {
  box-shadow: 2px 2px 5px #babecc, -2px -2px 5px #fff;
}
button:active {
  box-shadow: inset -1px -1px 2px #fff, inset 1px 1px 2px #babecc;
}
.NeuIconButton {
  width: fit-content;
  margin-bottom: 20px;
}
.NeuIconButton button {
  font-family: Nexa;
  font-weight: 900;
  letter-spacing: 2px;
  height: 50px;
  line-height: 23px;
  margin-bottom: 12px;
}
</style>
