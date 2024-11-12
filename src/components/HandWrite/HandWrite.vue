<template>
    <div class="hand-write-container" ref="ctn">

    </div>
</template>

<script lang="ts" setup>
import { onMounted, ref } from 'vue';

const ctn = ref<HTMLElement>();
window.ontouchmove = (event: TouchEvent) => {
    event.preventDefault();
};
onMounted(() => {
    let c = ctn.value as HTMLElement;
    c.addEventListener('pointermove', (event: PointerEvent) => {
        console.log(event.pressure);
    })
})
</script>
<style lang="less" scoped>
.hand-write-container {
    width: 100%;
    height: 100%;
}
</style>