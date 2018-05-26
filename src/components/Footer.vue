<template>
<el-row type="flex" justify="center" align="middle">
    <el-col>
    </el-col>
    <el-col :span="6" >
        <a href="https://instagram.com/hostelraduga" target="_blank">
            <el-button size="mini" circle icon="fab fa-instagram fa-2x"></el-button>
        </a>
    </el-col>
    <el-col :span="6">
        &copy; {{ this.years }}, Хостел &laquo;Радуга&raquo;
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