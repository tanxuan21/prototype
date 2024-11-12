<script setup lang="ts">
// 1.1 引入Vditor 构造函数
import Vditor from 'vditor'
// 1.2 引入样式
import 'vditor/dist/index.css';
import { ref, onMounted } from 'vue';

// 2. 获取DOM引用
const vditor = ref()
const vdtctn = ref<HTMLElement>();
// 3. 在组件初始化时，就创建Vditor对象，并引用
onMounted(() => {
    let el = (vdtctn.value as HTMLElement);
    console.log(el);
    new Vditor('vditor', {
        height: '100%',
        width: '100%',
        toolbarConfig: {
            hide: true,
        }
    })
})

</script>

<template>
    <!-- 指定一个容器 -->
    <div id="vditor" ref="vdtctn"></div>
</template>
