<template>
    <div style="height: 100%;">
        <el-container>
            <el-aside width="54px">
                <router-link to="/">Home</router-link> |
                <router-link to="/about">About</router-link>
            </el-aside>
            <el-main>
                <el-container>
                    <el-aside width="250px" class="proj-nav">

                    </el-aside>
                    <el-main class="proj-content">

                    </el-main>
                </el-container>


            </el-main>
        </el-container>
    </div>
    <router-view />
</template>

<script setup>
/**
 * 单独设置 <body> 的 margin: 0；这里已被 index.css 所替代
 * document.querySelector('body').setAttribute('style', 'margin: 0')
 */
import ProjNav from './components/ProjNav.vue';
</script>
<style lang="less">
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    position: fixed;
    height: 100%;
    width: 100%;
}

.el-container {
    height: 100%;

    .el-aside {
        height: 100%;
        background-color: #22253F;
    }

    .el-main {
        padding: 0;
        background-color: var(--el-bg-color-page);

        .proj-nav {
            background-color: var(--el-bg-color-page);
            border-right: 1px solid var(--el-border-color-dark);
        }
        .proj-content {
            background-color: var(--el-border-color-dark);
        }
    }
}

nav {
    // float: left;
    // width: 54px;
    // height: 100%;
    // background: #303133;

    a {
        font-weight: bold;
        color: #2c3e50;

        &.router-link-exact-active {
            color: #42b983;
        }
    }
}
</style>
