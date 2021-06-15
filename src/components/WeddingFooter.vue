<template>
    <footer>
        <slot></slot>
    </footer>
</template>

<script setup>

</script>

<style scoped>
    footer {
        display: flex;
        justify-content: center;
        padding: var(--padding) var(--padding) 12px var(--padding);
        font-size: 10px;
    }
    
</style>