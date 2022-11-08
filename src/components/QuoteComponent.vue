<template>
    <p>“{{quote}}”</p>
</template>
<script setup>
    const props = defineProps({
        quote : String
    })
</script>
<style>
    p {
        color: var(--lightCyan);
        text-align: center;
        font-weight: 800;
        font-size: 28px;
    }
</style>