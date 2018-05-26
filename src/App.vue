<template>
  <div id="app">
    <el-row type="flex" justify="center">
      <el-col><Reviews /></el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="20">
        <Map />
      </el-col>
    </el-row>
    <el-row type="flex" justify="center">
      <el-col :span="16">
        <Gallery />
      </el-col>
    </el-row>
  </div>
</template>

<script>
import Reviews from './components/Reviews.vue'
import Map from './components/Map.vue'
import Gallery from './components/Gallery.vue'

export default {
  name: 'app',
  components: {
    Map, Gallery, Reviews
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Caveat|Lora');
#app {
  font-family: 'Lora', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
