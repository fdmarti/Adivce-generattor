<template>
      <h1>{{title}}</h1>
</template>
<script setup>
const props = defineProps({
    title: String
})
</script>
<style>
    h1 {
        margin: 0;
        padding: 0;
        text-align: center;
        text-transform: uppercase;
        letter-spacing: 3px;
        font-weight: 500;
        font-size: 15px;
        color: var(--neonGreen);
    }
</style>