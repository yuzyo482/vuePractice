<template>
    <nav>
        <div>{{ title }}</div>
        <div>{{  subtitle }}</div>
    </nav>
</template>

<script setup>
    defineProps(["title" , "subtitle"]);
</script>

<style scoped>
    nav{padding: 10px;}
</style>