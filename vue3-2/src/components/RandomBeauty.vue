<template>
  <div>
      <h2>欢迎光临红浪漫洗浴中心</h2>
      <div>随机选择一位美女为你服务</div>
      <div v-if="loading">loading...</div>
      <img v-if="loaded" :src="result.imgUrl" alt="" />
  </div>
</template>

<script lang="ts">
// import { ref } from "vue";
import useUrlAxios from "../hooks/useUrlAxios";
const app = {
  name: "RandomBeauty",
  setup() {
     const { result, loading, loaded } = useUrlAxios("https://apiblog.jspang.com/default/getGirl");
     return { result, loading, loaded };
  },
};
export default app;
</script>

<style scoped>
img {
  width: 250px;
  height: 300px;
}
</style>

