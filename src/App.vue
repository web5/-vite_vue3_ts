<script setup lang="ts">
import { ref } from "vue";
import { NConfigProvider } from "naive-ui";
import { zhCN, darkTheme } from "naive-ui";
import type { GlobalTheme } from "naive-ui";
const theme = ref<GlobalTheme | null>(null);
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
// import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <n-config-provider :locale="zhCN" :theme="theme">
    <router-view></router-view>
  </n-config-provider>
</template>

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
