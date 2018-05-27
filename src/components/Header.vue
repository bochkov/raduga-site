<template>
<div>
  <div>
    <img src="../assets/logo.png" alt="Хостел Радуга" id="mainlogo" />
  </div>
    <el-row type="flex" align="top">
        <el-col :span="16">
        </el-col>
        <el-col class="icons" :span="8">
            <a href="https://instagram.com/hostelraduga" target="_blank">
                <el-button size="mini" circle icon="fab fa-instagram fa-2x"></el-button>
            </a>
            <a href="https://vk.com/raduga_hostelekb" target="_blank">
                <el-button size="mini" circle icon="fab fa-vk fa-2x"></el-button>
            </a>
            <a href="mailto:raduga-hostelekb@yandex.ru" target="_blank">
                <el-button size="mini" circle icon="fas fa-envelope fa-2x"></el-button>
            </a>
            <p class="subtitle-2 phone">
                +7 (912) 24-27-233
                <br/>
                +7 (912) 29-44-460
            </p>
        </el-col>
    </el-row>
</div>
</template>

<script>
export default {

}
</script>

<style>
#mainlogo {
  position: absolute;
  top: 20px;
  left: 10%;
  width: 200px;
  height: 200px;
}

.phone {
    color: #333;
}
</style>