<template>
    <img :src="result && result.imgUrl" alt="" />
</template>

<script lang="ts">
import axios from "axios"
import { defineComponent } from "vue"
export default defineComponent({
    async setup() {
       const rawData = await axios.get("https://apiblog.jspang.com/default/getGirl")
       return {result:rawData.data}
    }
})
</script>

<style scoped>
img {
    width: 250px;
    height: 300px;
}
</style>