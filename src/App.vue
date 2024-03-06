<script setup>
import { ref } from 'vue';
let state=ref({
  title: "網站標題",
  className: "title"
});
let handler=function(){
  state.value.title="new網站標題";
  state.value.className="newTitle";
};
</script>

<template>
  <nav>基本導覽列</nav>
  <main>
    <div :class="state.className">{{ state.title }}</div>
    <button @click="handler">按鈕</button>
  </main>
</template>

<style scoped>
.title{font-weight: bold;}
.newTitle{color: green;}
</style>
