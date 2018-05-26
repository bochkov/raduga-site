<template>
  <el-container id="app">
    <el-header height="220px">
      <Header />
    </el-header>
    <el-main>
      
      <Map />
      <Gallery />
      <Reviews />
    </el-main>
    <el-footer height="100px">
      <Footer />
    </el-footer>
  </el-container>
</template>

<script>
import Header from "./components/Header.vue";
import Reviews from "./components/Reviews.vue";
import Map from "./components/Map.vue";
import Gallery from "./components/Gallery.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    Map,
    Gallery,
    Reviews,
    Footer
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Caveat|Lora");
body {
  margin: 0;
}
#app {
  font-family: "Lora", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.celem {
  padding: 40px 0;
}
.el-header {
  text-align: center;
  font-size: 2em;
  padding: 0;
  background-color: coral;
}
.el-main {
  padding: 0;
  margin: 0;
}
.el-footer {
  padding: 0;
  margin: 0;
  background-color: #333;
}
</style>
