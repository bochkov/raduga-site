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
      title: "Хостел &laquo;Радуга&raquo;",
      subtitle: "Рады вам!"
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
      var ht = "";
      for (var i = 0; i < this.title.length; ++i) {
        var ch = this.title.charAt(i);
        if (ch === "&") {
          inHtml = true;
        }

        if (!inHtml)
          if (ch === " ") ret = ret + ch;
          else
            ret =
              ret +
              "<span style='color: " +
              this.getRandomColor() +
              ";'>" +
              ch +
              "</span>";
        else ht = ht + ch;
        if (inHtml && ch === ";") {
          inHtml = false;
        }
        if (!inHtml && ht.length) {
          ret =
            ret +
            "<span style='color: " +
            this.getRandomColor() +
            ";'>" +
            ht +
            "</span>";
          ht = "";
        }
      }
      return ret;
    }
  }
};
</script>

<style>
</style>