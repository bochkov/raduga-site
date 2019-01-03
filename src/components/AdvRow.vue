<template>
  <div class="adv">
    <div class="hidden-md-and-up">
      <el-row>
        <el-col>
          <img :src="img">
        </el-col>
      </el-row>
      <el-row>
        <el-col class="pad" v-html="text"/>
      </el-row>
    </div>
    <div class="hidden-sm-and-down">
      <el-row v-if="index % 2 == 0">
        <el-col :md="16" :lg="16" :xl="16" v-html="text"/>
        <el-col :md="8" :lg="8" :xl="8">
          <img :src="img">
        </el-col>
      </el-row>
      <el-row v-else>
        <el-col :md="8" :lg="8" :xl="8">
          <img :src="img">
        </el-col>
        <el-col :md="15" :lg="15" :xl="15" :offset="1" v-html="text"/>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {
  props: ["text", "img", "index"]
};
</script>

<style scoped>
img {
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.adv .hidden-md-and-up .el-row {
  padding: 0;
}
.adv .hidden-md-and-up .pad {
  padding: 20px;
}
.adv .hidden-sm-and-down .el-row {
  padding: 20px;
}
.adv .hidden-sm-and-down .el-col {
  padding: 10px 20px;
  vertical-align: top;
}
</style>