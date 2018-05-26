<template>
    <el-row id="carousel-row" type="flex" justify="center" class="celem">
        <el-col style="width: 1000px;">
            <el-carousel :interval="10000" trigger="click" height="600px" indicator-position="outside">
                <el-carousel-item v-for="index in 10" :key="index">
                    <span class="img-title">title {{index}}</span>
                    <img :src="rurl(index)" />
                </el-carousel-item>
            </el-carousel>
        </el-col>
    </el-row>
</template>

<script>
export default {
  methods: {
    rurl: function(idx) {
      var ret = 
        "https://fakeimg.pl/1000x600/333/cccc00?text=Raduga+" +
        idx +
        "&font=lobster";
        return ret;
    }
  },
  data() {
    return {
      images: [
        {
          url: "",
          title: "title 1"
        },
        {
          url: "",
          title: "title 2"
        },
        {
          url: "",
          title: "title 3"
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