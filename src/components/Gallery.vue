<template>
    <el-row id="carousel-row" type="flex" justify="center" class="celem">
        <el-col :xl="6" :lg="6" :md="6" :sm="8">
            <el-carousel :interval="10000" trigger="click" height="500px" indicator-position="outside">
                <el-carousel-item v-for="(image, index) in images" :key="index">
                    <img align="center" :src="image" />
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
            "https://fakeimg.pl/855x500/a3a3a3/333?text=Raduga+1&font=lobster",
            "https://fakeimg.pl/855x500/a3a3a3/333?text=Raduga+2&font=lobster",
            "https://fakeimg.pl/855x500/a3a3a3/333?text=Raduga+3&font=lobster",
        ]
    };
  }
};
</script>

<style scope>
#carousel-row {
  background-color: aquamarine;
}
</style>