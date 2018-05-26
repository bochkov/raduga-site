<template>
    <div id="reviews">
        <el-row type="flex" :gutter="20" justify="center">
            <el-col :span="7">
                <el-rate v-model="rate1" disabled text-color="#ff9900"></el-rate>
                <div class="cite">Гостиница - говно. Кроватей мало. Ночевали на коврике!</div>
                <div class="author">Недовольный посетитель</div>
            </el-col>
            <el-col :span="7">
                <el-rate v-model="rate2" disabled text-color="#ff9900"></el-rate>
                <div class="cite">Гостиница - говно. Кроватей мало. Ночевали на коврике!</div>
                <div class="author"><a href="#">Вася</a></div>
            </el-col>
            <el-col :span="7">
                <el-rate v-model="rate3" disabled text-color="#ff9900"></el-rate>
                <div class="cite">Гостиница - говно. Кроватей мало. Ночевали на коврике!</div>
                <div class="author">Федя</div>
            </el-col>
        </el-row>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                rate1: 1,
                rate2: 5,
                rate3: 4
            }
        }
    }
</script>

<style scope>
#reviews {
    font-family: 'Caveat', sans-serif;
    font-size: 20pt;
}
.author {
    text-align: right;
}
</style>