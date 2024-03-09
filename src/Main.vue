<script setup>
    import {ref} from "vue";
    let text = ref("網站內容");
    let change = function(){
        text.value = "New網站內容";
    };
    defineProps(["color","backgroundColor"]);
    let emit = defineEmits(["update"]);
    let updateParentSubtitle = function(){
        emit("update");
    };
</script>

<template>
    <main style="{color:color, background-color: backgroundColor}">
        <div @click="change">{{ text }}</div>
        <button @click="updateParentSubtitle">CHANGE!</button>
    </main>
</template>

<style scoped>
    main{
        padding:10px;
        background-color: green;
    }
</style>