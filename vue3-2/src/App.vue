<template>
  <div>
    <div>{{nowTime}}</div>
    <div><button @click="getNowTime">显示时间</button></div>
    <Beauty></Beauty>
  </div>
</template>

<script lang="ts">
// import { ref } from "vue";
import { nowTime, getNowTime } from './hooks/useNowTime';
import Beauty from '@/components/RandomBeauty.vue';  //随机出现美女组件
const app = {
  name: "App",
  components: {
    Beauty
  },
  setup() {
    //  const nowTime = ref("00:00:00");
    //  const getNowTime = () => {
    //    const now = new Date();
    //    const hour = now.getHours() < 10 ? "0" + now.getHours() : now.getHours();
    //    const minu = now.getMinutes() < 10 ? "0" + now.getMinutes() : now.getMinutes();
    //    const sec = now.getSeconds() < 10 ? "0" + now.getSeconds() : now.getSeconds();
    //    nowTime.value = hour + ":" + minu + ":" + sec;
    //    setTimeout(getNowTime, 1000);
    //  };
     return {
       nowTime,
       getNowTime
     }
  },
};
export default app;
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
