<template>
    <el-row id="reviews" class="celem" type="flex" :gutter="10" justify="center">
        <el-col :xl="8" :lg="8" :md="8" :sm="20" :xs="20"
          v-for="(review, index) in reviews" :key="index">
          <el-card class="box-card">
            <el-rate class="rating" v-model="review.rating" disabled text-color="#ff9900"></el-rate>
            <div class="cite">{{review.text}}</div>
            <div class="author">
                <a v-if="review.url && review.url.length" :href="review.url" target="_blank">
                {{review.author}}
                </a>
                <span v-else>{{review.author}}</span>
                &nbsp;
                <i class="far fa-user fa-sm"></i>
            </div>
          </el-card>
        </el-col>
    </el-row>
</template>

<script>
export default {
  data() {
    return {
      reviews: [
        {
          author: "Федя",
          url: "http://flamp.ru",
          text: "Гостиница - говно. Кроватей мало. Ночевали на коврике!",
          rating: 1
        },
        {
          author: "Вася",
          url: "",
          text: "Гостиница - говно. Кроватей мало. Ночевали на коврике!",
          rating: 5
        },
        {
          author: "Недовольный посетитель",
          url: "",
          text: "Гостиница - говно. Кроватей мало. Ночевали на коврике!",
          rating: 4
        }
      ]
    };
  }
};
</script>

<style scope>
#reviews {
  font-family: "Caveat", sans-serif;
  font-size: 1.5em;
  background-color: azure;
  padding-left: 10px;
  padding-right: 10px;
}
.author {
  text-align: right;
  font-size: 0.8em;
  padding: 5px;
}
.rating {
  text-align: center;
  padding: 10px;
}
.box-card {
  min-width: 300px;
}
</style>