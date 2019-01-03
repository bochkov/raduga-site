<template>
  <div id="gallery-row">
    <el-row v-if="mode == 'carousel'" type="flex" justify="center" class="celem">
      <el-col style="width: 1000px;">
        <el-carousel :interval="10000" trigger="click" height="650px" indicator-position="outside">
          <el-carousel-item v-for="(image, index) in images" :key="index">
            <div v-html="image.title"></div>
            <img :src="image.url">
          </el-carousel-item>
        </el-carousel>
      </el-col>
    </el-row>
    <el-row v-else>
      <div class="img-list" v-for="(image, index) in images" :key="index">
        <img :src="image.url">
        <span v-html="image.title"></span>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {
  props: ["mode"],
  data() {
    return {
      images: [
        {
          url: require("@/assets/gal6.png"),
          title: ""
        },
        {
          url: require("@/assets/gal7.png"),
          title: ""
        },
        {
          url: require("@/assets/gal8.png"),
          title: ""
        },
        {
          url: require("@/assets/gal9.png"),
          title: ""
        },
        {
          url: require("@/assets/gal10.png"),
          title: ""
        },
        {
          url: require("@/assets/gal11.png"),
          title: "Зона ресепшн"
        },
        {
          url: require("@/assets/gal12.png"),
          title: "Зона ресепшн"
        },
        {
          url: require("@/assets/gal13.png"),
          title: "Санузел"
        },
        {
          url: require("@/assets/gal14.png"),
          title: "На нашей кухне"
        },
        {
          url: require("@/assets/gal15.png"),
          title: "На нашей кухне"
        },
        {
          url: require("@/assets/gal16.png"),
          title: "На нашей кухне"
        },
        {
          url: require("@/assets/gal17.png"),
          title: "Различные игры для досуга"
        },
        {
          url: require("@/assets/gal18.png"),
          title: "Различные игры для досуга"
        },
        {
          url: require("@/assets/gal19.png"),
          title: "Окна балкона выходят на тихую улочку"
        },
        {
          url: require("@/assets/gal5.png"),
          title: "В пяти минутах ходьбы - &laquo;Екатеринбург-Арена&raquo;"
        }
      ]
    };
  }
};
</script>

<style>
#gallery-row {
  background-color: #eaffed;
}

.el-carousel {
  text-align: center;
  font-size: 1.1em;
}
.el-carousel img {
  height: 100%;
}

.img-list {
  margin: 40px 0;
  text-align: center;
  font-size: 0.9em;
}
.img-list img {
  width: 100%;
}
</style>