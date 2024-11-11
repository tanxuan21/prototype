<template>
    <div class="text-container">
        <TODO></TODO>
    </div>
</template>
<script lang="ts" setup>
import { TODO } from './Components.ts';
</script>

<style scoped>
.text-container {
    width: 80vw;
    height: 80vh;
    background: #000;
    border-radius: 10px;
    overflow: hidden;
}
</style>