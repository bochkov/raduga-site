<template>
  <el-container id="app">
    <el-header height="800px">
      <Header />
    </el-header>
    <el-main>
      <Advantage />
      <About />
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
import Book from "./components/Book.vue";
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
    Book,
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
@import url("https://fonts.googleapis.com/css?family=Caveat|Bad+Script|Marck+Script|Lora|Playfair+Display+SC");
body {
  margin: 0;
}
#app {
  font-family: "Lora", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.celem {
  padding: 20px 20px;
}
.el-header {
  text-align: center;
  padding: 0;
  padding-top: 40px;
  background-image: url("./assets/mainpic.png");
  background-repeat: no-repeat;
  background-size: cover;
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
  text-align: left;
}
.title {
  font-family: "Playfair Display SC", sans-serif;
  font-size: 5em;
  font-weight: bolder;
}
.title-2 {
  font-size: 2em;
  text-align: center;
}
.subtitle-2 {
  font-size: 1.2em;
  text-align: center;
}
.subtitle {
  font-size: 2.5em;
  text-align: center;
}
.el-button {
  margin: 5px 5px;
}
</style>
