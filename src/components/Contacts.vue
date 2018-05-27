<template>
<el-row id="contacts-row" type="flex" class="celem" justify="space-around">
    <el-col :span="20">
        <el-row type="flex" justify="center">
            <el-col v-for="(contact, index) in this.contacts" :key="index">
                <div class="contact">
                    <i :class='contact.icon' :style='contact.style' class="muted-icon fa-2x"></i>
                    <p/>
                    <span v-html="contact.text"></span>
                </div>
            </el-col>
        </el-row>
    </el-col>
</el-row>
</template>

<script>
export default {
    data: function() {
        return {
            contacts: [
                {
                    icon: 'fas fa-map-marker-alt',
                    text: 'Екатеринбург, ул. Крауля, д. 2<br/>(вход со стороны перекрестка Крауля-Крылова)',
                    style: 'color: darkred;'
                },
                {
                    icon: 'fas fa-phone',
                    text: '+7 (912) 242-72-33',
                    style: 'color: darkgreen;'
                },
                {
                    icon: 'fas fa-credit-card',
                    text: 'Расчет по картам<br/>Наличный расчет',
                    style: 'color: #333;'
                }
            ]
        }
    }
}
</script>

<style>
.contact {
    text-align: center;
}
</style>