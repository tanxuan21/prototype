<template>
    <div id="my-monaco-container" style="width: 500px;height: 500px;text-align: left" ref="mncctn"></div>
</template>

<script lang="ts" setup>
import * as monaco from 'monaco-editor'
import { onMounted, ref } from 'vue';
const mncctn = ref<HTMLElement>();
onMounted(() => {

    monaco.editor.create(mncctn.value as HTMLElement, {
        value: ['function x() {', '\tconsole.log("Hello world!");', '}'].join('\n'),
        language: 'javascript'
    });
})

</script>