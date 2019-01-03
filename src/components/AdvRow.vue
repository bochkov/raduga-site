<template>
  <el-row :gutter="20" v-if="index % 2 == 0">
    <el-col class="hidden-md-and-up" :md="8" :lg="8" :xl="8">
      <img :src="img">
    </el-col>
    <el-col :md="16" :lg="16" :xl="16" v-html="text"/>
    <el-col class="hidden-sm-and-down" :md="8" :lg="8" :xl="8">
      <img :src="img">
    </el-col>
  </el-row>
  <el-row :gutter="20" v-else>
    <el-col :md="8" :lg="8" :xl="8">
      <img :src="img">
    </el-col>
    <el-col :md="16" :lg="16" :xl="16" v-html="text"/>
  </el-row>
</template>

<script>
export default {
  props: ["text", "img", "index"]
};
</script>

<style>
img {
    display: block;
    margin-left: auto;
    margin-right: auto;
}
.el-row {
    padding: 10px 10px;
}
.el-col {
    padding: 10px 20px;
    vertical-align: top;
}
</style>