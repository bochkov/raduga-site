<template>
    <el-row type="flex" align="top">
        <el-col :span="20">
            <div class="title" v-html="this.coloredTitle"></div>
            <div class="subtitle" v-html="this.subtitle"></div>
        </el-col>
        <el-col class="icons" :span="4">
            <a href="https://instagram.com/hostelraduga" target="_blank">
                <el-button size="small" circle icon="fab fa-instagram fa-2x"></el-button>
            </a>
        </el-col>
    </el-row>
</template>

<script>
export default {
  data() {
    return {
      title: "Хостел Радуга",
      subtitle: "Рады вам!",
    };
  },
  methods: {
    getRandomColor: function() {
      var letters = "0123456789ABCDEF";
      var color = "#";
      for (var i = 0; i < 6; i++) {
        color += letters[Math.floor(Math.random() * 16)];
      }
      return color;
    }
  },
  computed: {
    coloredTitle: function() {
      var inHtml = false;
      var ret = "";
      for (var i = 0; i < this.title.length; ++i) {
        ret =
          ret +
          "<span style='color: " +
          this.getRandomColor() +
          ";'>" +
          this.title.charAt(i) +
          "</span>";
      }
      return ret;
    }
  }
};
</script>

<style>
</style>