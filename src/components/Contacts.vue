<template>
  <el-row id="contacts-row">
    <el-col v-for="contact in this.contacts" :key="contact.index" :md="8" :lg="8" :xl="8">
      <div class="contact">
        <i :class="contact.icon" :style="contact.style" class="muted-icon fa-2x"></i>
        <p/>
        <span :style="contact.text_style" v-html="contact.text"/>
      </div>
    </el-col>
  </el-row>
</template>

<script>
export default {
  data: function() {
    return {
      contacts: [
        {
          index: 0,
          icon: "fas fa-credit-card",
          text: "Расчет по картам<br/>Наличный расчет",
          style: "color: #333;"
        },
        {
          index: 1,
          icon: "fas fa-map-marker-alt",
          text:
            "Екатеринбург, ул. Крауля, д. 2<br/>(вход со стороны перекрестка Крауля-Крылова)",
          style: "color: darkred;"
        },
        {
          index: 2,
          icon: "fas fa-phone",
          text: "+7 (912) 24-27-233",
          style: "color: darkgreen;",
          text_style: "font-family: Overpass Mono; font-size: 0.9em"
        }
      ]
    };
  }
};
</script>

<style>
.contact {
  text-align: center;
  padding: 20px;
}
</style>