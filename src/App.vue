<script setup>
import { ref } from 'vue';
import NavComp from './Nav.vue'
import MainComp from './Main.vue'
let subtitle = ref("這是網站標題");
let updateSubtitle = function(){
  subtitle.value = "New網站標題";
};
</script>

<template>
  <NavComp 
    title="網站標題列"
    v-bind:subtitle="subtitle"
    ></NavComp>
  <MainComp
    color="white"
    background-color="black"
    @update="updateSubtitle"
    >
  </MainComp>
</template>

<style scoped>
</style>
