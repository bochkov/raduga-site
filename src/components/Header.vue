<template>
  <el-row id="header-row">
    <el-col id="logo-col" class="hidden-xs-only" :xs="12" :sm="15" :md="17" :lg="18" :xl="19">
      <img :src="logo" alt="Хостел Радуга" id="mainlogo">
    </el-col>
    <el-col :sm="8" :md="6" :lg="5" :xl="4" class="icons">
      <a href="https://instagram.com/hostelraduga" target="_blank">
        <el-button size="mini" circle icon="fab fa-instagram fa-2x"></el-button>
      </a>
      <a href="https://vk.com/raduga_hostelekb" target="_blank">
        <el-button size="mini" circle icon="fab fa-vk fa-2x"></el-button>
      </a>
      <a href="mailto:raduga-hostelekb@yandex.ru" target="_blank">
        <el-button size="mini" circle icon="fas fa-envelope fa-2x"></el-button>
      </a>
      <p class="subtitle-2 phone">+7 (912) 24-27-233
      </p>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data() {
    return {
      logo: require("@/assets/logo.png")
    };
  }
};
</script>

<style>
#header-row {
    padding: 0 20px;
}
#logo-col {
  padding-left: 5em;
  text-align: left;
}
#mainlogo {
  width: 200px;
  height: 200px;
}

.phone {
  color: #222;
  font-family: "Overpass Mono";
}

.icons {
  text-align: center;
  padding-top: 20px;
  border-radius: 5px;
  background-color: rgba(230, 236, 240, 0.85);
}
</style>