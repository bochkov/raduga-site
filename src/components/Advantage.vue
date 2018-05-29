<template>
<el-row id="adv-row" type="flex" class="celem" justify="center">
    <el-col :span="20">
        <div class="subtitle">
            Добро пожаловать!
        </div>
        <div class="title-2">
            Будем рады видеть вас в нашем хостеле.<br/>
        </div>
        <div class="text">
            <el-row class="celem" justify="space-beween" type="flex">
                <el-col :xs="24" :sm="24" :md="24" :lg="16" :xl="16">
                    <span class="subtitle-2">Расположение</span>
                    <p>
                        &laquo;Радуга&raquo; находится недалеко от центра города в 5 минутах ходьбы от &laquo;Екатеринбург-Арены&raquo;. 
                        Хостел славится не только своим уютом и гостеприимством, 
                        но и замечательным расположением относительно основных элементов современной инфраструктуры города.
                    </p>
                </el-col>
                <el-col class="hidden-xs-only" :xs="23" :sm="23" :md="7" :lg="7" :xl="7" :offset="1">
                    <img src="../assets/adv1.png"/>
                </el-col>
            </el-row>
            <el-row class="celem" type="flex" justify="space-between">
                <el-col class="hidden-xs-only" :xs="24" :sm="24" :md="8" :lg="8" :xl="8">
                    <img src="../assets/adv2.png"/>
                </el-col>
                <el-col  :xs="23" :sm="23" :md="15" :lg="15" :xl="15" :offset="1">
                    <span class="subtitle-2">Наши услуги</span>
                    <p>
                        Мы предоставялем высокий уровень комфорта. В вашем распоряжении сейф, 
                        стиральная машина, утюг и гладильная доска. 
                    </p>
                    <p>
                        Настольные игры и книги помогут скрасить досуг. 
                        Также у нас в продаже большой выбор сувениров и действует гибкая система скидок.
                    </p>
                </el-col>
            </el-row>
            <el-row class="celem" type="flex" justify="space-between">
                <el-col :xs="24" :sm="24" :md="24" :lg="16" :xl="16">
                    <span class="subtitle-2">Комфорт и уют</span>
                    <p>
                        Хостел располагает тремя номера с двухъярусными кроватями, которые придутся на вкус любому путешественнику.
                        Возле каждой кровати есть индивидуальная розетка.
                        Бесплатный Wi-Fi на всей территории хостела.
                    </p>
                    <p>
                        В хостеле имеется оборудованная общая кухня со всей необходимой техникой для самостоятельного приготовления пищи. На кухне имеется варочная поверхность, холодильник, микроволновая печь. 
                    </p>
                    <p>
                        Имеются 2 санузла с душевыми кабинами, а также стиральная машина, фен и гладильная доска с утюгом. Гостям бесплатно предоставляются необходимые гигиенические средства.
                    </p>
                </el-col>
                <el-col class="hidden-xs-only" :xs="23" :sm="23" :md="7" :lg="7" :xl="7" :offset="1">
                    <img src="../assets/adv3.png"/>
                </el-col>
            </el-row>
        </div>
    </el-col>
</el-row>
</template>

<style>
#adv-row {
    background-color: #eaffed;
}
</style>