<template>
    <el-row id="carousel-row" type="flex" justify="center" class="celem hidden-sm-and-down">
        <el-col style="width: 1000px;">
            <el-carousel :interval="10000" trigger="click" height="600px" indicator-position="outside">
                <el-carousel-item v-for="(image, index) in images" :key="index">
                    <span class="img-title" v-html="image.title"></span>
                    <img :src="image.url" />
                </el-carousel-item>
            </el-carousel>
        </el-col>
    </el-row>
</template>

<script>
export default {
  data() {
    return {
      images: [
        {
          url: require("../assets/gal5.png"),
          title: "В пяти минутах ходьбы - &laquo;Екатеринбург-Арена&raquo;"
        },
        {
          url: require("../assets/gal4.png"),
          title: "Розовая комната"
        },
        {
          url: require("../assets/gal1.png"),
          title: "Желтая комната"
        },
        {
          url: require("../assets/gal3.png"),
          title: "В одной из комнат"
        }
      ]
    };
  }
};
</script>

<style>
#carousel-row {
  background-color: #eaffed;
}
.img-title {
  font-size: 1.5em;
}
</style>