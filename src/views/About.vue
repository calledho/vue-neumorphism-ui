<template>
  <div class="about">
    <h1>This is an about page</h1>
    <NeuProgress />
    <NeuProgress type="hot" />
    <NeuCircleProgress
      dashoffset="100"
      style="left:50%;transform:translateX(-50%);top:10px"
    />
  </div>
</template>

<script>
// @ is an alias to /src
import NeuProgress from "@/components/NeuProgress.vue";
import NeuCircleProgress from "@/components/NeuCircleProgress.vue";
export default {
  name: "Home",
  components: {
    NeuProgress,
    NeuCircleProgress
  }
};
</script>

<style scoped>
.about {
  width: 500px;
  margin: 0 auto;
}
</style>
