<template>
  <el-container id="app">
    <el-header height="800px">
      <Header />
    </el-header>
    <el-main>
      <About />
      <Advantage />
      <Gallery />
      <Map />
      <Reviews />
      <Contacts />
    </el-main>
    <el-footer height="100px">
      <Footer />
    </el-footer>
  </el-container>
</template>

<script>
import Header from "./components/Header.vue";
import About from "./components/About.vue";
import Advantage from "./components/Advantage.vue";
import Reviews from "./components/Reviews.vue";
import Map from "./components/Map.vue";
import Gallery from "./components/Gallery.vue";
import Contacts from "./components/Contacts.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    About,
    Advantage,
    Map,
    Gallery,
    Reviews,
    Contacts,
    Footer
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Caveat|Lora");
body {
  margin: 0;
}
dt {
  font-weight: bold;
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
  padding: 0;
  padding-top: 40px;
  background-color: #ddffaa;
}
.el-main {
  padding: 0;
  margin: 0;
}
.el-footer {
  padding: 10px 0;
  margin: 0;
  background-color: #4f424a;
  color: white;
}
.text {
  font-size: 1.5em;
  text-align: justify;
}
.title {
  font-size: 3em;
}
.title-2 {
  font-size: 2em;
}
.subtitle {
  font-size: 1.2em;
}
.el-button {
  margin: 5px 5px;
}
</style>
