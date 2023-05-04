<template>
    <!-- <div>
        <ProjNav></ProjNav>
    </div> -->
</template>

<script setup>
import { reactive, ref, createApp } from "vue";
/* 组件局部注册 */
const app = createApp({});
import ProjNav from "@/components/ProjNav.vue";
app.component({
    ProjNav,
});

</script>

<style lang="less" scoped></style>