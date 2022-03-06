<template>
  <div class="login">Login</div>
  <div>用户名:{{ mainStore.name }}<br />长度:{{ mainStore.nameLength }}</div>
  <hr />
  <button @click="updateName">修改store中的name</button>
  <n-button>naive-ui</n-button>
</template>
<script setup lang="ts">
import { useMainStore } from "@/store/main";
import { NButton } from "naive-ui";

console.log(import.meta.env.NODE_ENV);

const mainStore = useMainStore();

const updateName = () => {
  // $patch 修改 store 中的数据
  mainStore.$patch({
    name: "名称被修改了,nameLength也随之改变了",
  });
};
</script>

<style scoped lang="scss">
.login {
  font-size: 20px;
}
</style>
