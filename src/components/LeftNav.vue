<template>
    <nav>
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link>
    </nav>
</template>

<script setup>
// 设置 <body> 的 margin: 0；
document.querySelector('body').setAttribute('style', 'margin: 0')
</script>

<style lang="less" scoped>
nav {
    width: 54px;
    height: 100%;
    background: #000;

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>