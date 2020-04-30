<template>
  <div class="home">
    <NeuText>FOPartform</NeuText>
    <div class="comment">
      <neu-card style="width:40%;min-width:250px;margin:0 auto;">
        <neu-input
          class="comment"
          style="margin-top:60px"
          icon="iconfont icon-bussiness-man"
          placeholder="输入用户名"
        />
        <neu-input
          type="password"
          class="comment"
          icon="iconfont icon-Notvisible"
          placeholder="输入密码"
        />
        <neu-button class="comment" name="Login" />
      </neu-card>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NeuButton from "@/components/NeuButton.vue";
import NeuInput from "@/components/NeuInput.vue";
import NeuCard from "@/components/NeuCard.vue";
import NeuText from "@/components/NeuText.vue";
//import NeuIconButton from "@/components/NeuIconButton.vue";
export default {
  name: "Home",
  components: {
    NeuButton,
    NeuInput,
    NeuCard,
    NeuText
    //NeuIconButton
  }
};
</script>

<style scoped>
@import "../assets/iconfont/iconfont.css";
.home {
  width: 99%;
  margin: 0 auto;
}
.comment {
  margin: 40px auto;
}
</style>
