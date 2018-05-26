<template>
    <el-row id="carousel-row" type="flex" justify="center" class="celem">
        <el-col style="width: 1000px;">
            <el-carousel :interval="10000" trigger="click" height="700px" indicator-position="outside">
                <el-carousel-item v-for="(image, index) in images" :key="index">
                    <span class="img-title">{{image.title}}</span>
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
                url: "https://fakeimg.pl/1000x700/333/cccc00?text=Raduga+1&font=lobster",
                title: 'title 1'
            },
            {
                url: "https://fakeimg.pl/1000x700/333/cccc00?text=Raduga+2&font=lobster",
                title: 'title 2'
            },
            {
                url: "https://fakeimg.pl/1000x700/333/cccc00?text=Raduga+3&font=lobster",
                title: 'title 3'
            }
        ]
    };
  }
};
</script>

<style>
#carousel-row {
  background-color: #ddffaa;
}
.img-title {
    font-size: 1.5em;
}
</style>