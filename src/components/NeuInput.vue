<template>
  <div class="NeuInput">
    <input :type="type" :placeholder="placeholder" :value="value" />
    <template v-if="icon">
      <i :class="icon"></i>
    </template>
  </div>
</template>

<script>
export default {
  name: "NeuInput",
  props: {
    type: {
      type: String,
      default: "text"
    },
    placeholder: {
      type: String,
      default: ""
    },
    value: {
      type: String,
      default: ""
    },
    icon: {
      type: String,
      default: ""
    }
  }
};
</script>

<style scoped>
input {
  color: #868a9a;
  padding: 16px;
  background-color: #ebecf0;
  text-shadow: 1px 1px 0 #fff;
  font-size: 16px;
  border-radius: 320px;
  width: 100%;
  border: none;
  outline: none;
}
input::placeholder {
  color: #babecc;
}
.NeuInput {
  width: 100%;
  max-width: 300px;
}
.NeuInput {
  position: relative;
}

.NeuInput i {
  position: absolute;
  font-weight: bolder;
  color: #babecc;
  text-shadow: 1px 1px 0 #fff;
  top: 9px;
  right: 24px;
  font-size: 30px;
}

.NeuInput input {
  box-sizing: border-box;
  box-shadow: inset 2px 2px 6px #babecc, inset -4px -5px 8px #fff;
  transition: all 0.2s ease-in-out;
}

.NeuInput input:focus {
  box-shadow: inset 1px 1px 2px #babecc, inset -1px -1px 2px #fff;
}
</style>
