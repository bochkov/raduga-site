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
          url: require("../assets/gal6.png"),
          title: ""
        },
        {
          url: require("../assets/gal7.png"),
          title: ""
        },
        {
          url: require("../assets/gal8.png"),
          title: ""
        },
        {
          url: require("../assets/gal9.png"),
          title: ""
        },
        {
          url: require("../assets/gal10.png"),
          title: ""
        },
        {
          url: require("../assets/gal11.png"),
          title: "Зона ресепшн"
        },
        {
          url: require("../assets/gal12.png"),
          title: "Зона ресепшн"
        },
        {
          url: require("../assets/gal13.png"),
          title: "Санузел"
        },
        {
          url: require("../assets/gal14.png"),
          title: "На нашей кухне"
        },
        {
          url: require("../assets/gal15.png"),
          title: "На нашей кухне"
        },
        {
          url: require("../assets/gal16.png"),
          title: "На нашей кухне"
        },
        {
          url: require("../assets/gal17.png"),
          title: "Различные игры для досуга"
        },
        {
          url: require("../assets/gal18.png"),
          title: "Различные игры для досуга"
        },
        {
          url: require("../assets/gal19.png"),
          title: "Окна балкона выходят на тихую улочку"
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