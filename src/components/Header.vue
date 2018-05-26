<template>
    <el-row type="flex" align="top">
        <el-col :span="20">
            <div class="title" v-html="this.title"></div>
            <div class="subtitle" v-html="this.subtitle"></div>
        </el-col>
        <el-col class="icons" :span="4">
            <a href="https://instagram.com/hostelraduga" target="_blank">
                <el-button size="small" circle icon="fab fa-instagram fa-2x"></el-button>
            </a>
            <a href="https://instagram.com/hostelraduga" target="_blank">
                <el-button size="small" circle icon="fab fa-facebook fa-2x"></el-button>
            </a>
            <a href="https://instagram.com/hostelraduga" target="_blank">
                <el-button size="small" circle icon="fab fa-vk fa-2x"></el-button>
            </a>
        </el-col>
    </el-row>
</template>

<script>
export default {
    data() {
        return {
            title: 'Хостел &laquo;Радуга&raquo;',
            subtitle: 'Рады вам!'
        }
    }
}
</script>

<style>
</style>