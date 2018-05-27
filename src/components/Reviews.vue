<template>
    <el-row id="reviews" type="flex" class="celem hidden-xs-only" align="middle" justify="space-around">
        <el-col :xs="22" :sm="22" :md="12" :lg="6" :xl="6"
          v-for="(review, index) in reviews" :key="index">
          <el-card class="box-card">
            <el-rate class="rating" v-model="review.rating" disabled text-color="#ff9900"></el-rate>
            <div class="cite">{{review.text}}</div>
            <div class="author">
                <a v-if="review.url && review.url.length" :href="review.url"
                  class="link" target="_blank">{{review.author}}</a>
                <span v-else>{{review.author}}</span>
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
        },
        {
          author: "Довольный посетитель",
          url: "",
          text: "А нам понравилось! Все рядом, все под рукой. Вежливый персонал.",
          rating: 5
        }
      ]
    };
  }
};
</script>

<style scoped>
#reviews {
  font-family: "Caveat", sans-serif;
  font-size: 1.2em;
  background-color: #eaffed;
}
.author {
  text-align: right;
  font-size: 1em;
  padding-top: 20px;
}
.rating {
  text-align: center;
  padding-bottom: 20px;
}
.box-card {
  margin: 0 20px;
}
</style>