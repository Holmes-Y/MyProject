<template>
    <div>
        <el-button type="primary" @click="dialogFormVisible = true">添加项目</el-button>
        <el-dialog v-model="dialogFormVisible" title="添加项目">
            <el-form :model="form">
                <el-form-item label="项目名称" :label-width="formLabelWidth">
                    <el-input v-model="form.name" autocomplete="off" />
                </el-form-item>
                <el-form-item label="应用类型" :label-width="formLabelWidth">
                    <el-select v-model="form.region" placeholder="请选择应用类型">
                        <el-option label="" value="APP" />
                        <el-option label="" value="小程序" />
                    </el-select>
                </el-form-item>
                <el-form-item label="项目简介" :label-width="formLabelWidth">
                    <el-input v-model="form.desc" autocomplete="off" />
                </el-form-item>
            </el-form>
            <template #footer>
                <span class="dialog-footer">
                    <el-button @click="dialogFormVisible = false">取消</el-button>
                    <el-button type="primary" @click="dialogFormVisible = false">
                        确认
                    </el-button>
                </span>
            </template>
        </el-dialog>
    </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const dialogFormVisible = ref(false)
const formLabelWidth = '140px'

const form = reactive({
    name: '',
    region: '',
    desc: '',
})
</script>

<style lang="less" scoped>
.el-select {
    width: 300px;
}

.el-input {
    width: 300px;
}

.dialog-footer button:first-child {
    margin-right: 10px;
}
</style>