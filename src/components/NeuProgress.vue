<template>
  <div class="NeuProgress">
    <span :class="'.' + type"></span>
  </div>
</template>

<script>
export default {
  name: "NeuProgress",
  props: {
    type: {
      type: String,
      default: "cold"
    }
  }
};
</script>

<style scoped>
.NeuProgress {
  width: 500px;
  margin: 20px auto;
}
.NeuProgress span {
  color: black;
  font-size: 18px;
  position: relative;
  display: inline-block;
  width: 200px;
}
.NeuProgress span::before,
.NeuProgress span::after {
  content: "";
  display: block;
  height: 23px;
  width: 100%;
  background-color: #1f4a59;
  position: absolute;
  bottom: -20px;
  border-radius: 20px;
}
.NeuProgress span::before {
  background-color: #ebecf0;
  box-shadow: inset 2px 2px 6px #babecc, inset -4px -5px 8px #fff;
}
.NeuProgress span::after {
  height: 17px;
  bottom: -17px;
  left: 3px;
  background-image: linear-gradient(90deg, #0fbcf9, #34e7e4) !important;
  animation-duration: 1.2s;
  animation-fill-mode: forwards;
  animation-timing-function: ease-in-out;
}
.NeuProgress span::after {
  animation-name: mygress;
}
@keyframes mygress {
  from {
    width: 0;
  }
  to {
    width: 80%;
  }
}

.NeuProgress .hot::after {
  background-image: linear-gradient(90deg, #ff5733, #c70039) !important;
}
.NeuProgress .cold::after {
  background-image: linear-gradient(90deg, #0fbcf9, #34e7e4) !important;
}
</style>
