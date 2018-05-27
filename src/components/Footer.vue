<template>
<el-row type="flex" justify="center" align="middle">
    <el-col :offset="2" :span="10">
        &copy; {{ this.years }}, Хостел &laquo;Радуга&raquo;
    </el-col>
    <el-col :span="12">
        <a href="https://instagram.com/hostelraduga" target="_blank">
            <el-button size="mini" circle icon="fab fa-instagram fa-2x"></el-button>
        </a>
        <a href="https://vk.com/raduga_hostelekb" target="_blank">
            <el-button size="small" circle icon="fab fa-vk fa-2x"></el-button>
        </a>
        <a href="mailto:raduga-hostelekb@yandex.ru" target="_blank">
            <el-button size="mini" circle icon="fas fa-envelope fa-2x"></el-button>
        </a>
    </el-col>
</el-row>
</template>

<script>
export default {
    computed: {
        years: function() {
            return new Date().getFullYear();
        }
    }
}
</script>

<style>
</style>