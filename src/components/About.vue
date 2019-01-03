<template>
  <el-row id="about-row" class="celem">
    <el-col>
      <div class="title-2"></div>
      <div class="text">
        <span class="subtitle-2">Стоимость проживания - от 449 ₽ в сутки.</span>
        <div class="ulist">
          <span class="list-title">Бесплатно:</span>
          <ul>
            <li>Варочная плитка и микроволновая печь</li>
            <li>Холодильник</li>
            <li>Утюг и гладильная доска</li>
            <li>Настольные игры, книги</li>
            <li>Вызов такси</li>
          </ul>
        </div>
        <div class="ulist">
          <span class="list-title">Платно:</span>
          <ul>
            <li>Сейф</li>
            <li>Стиральная машина</li>
          </ul>
        </div>
        <div class="ulist">
          <span class="list-title">В хостеле действует гибкая система скидок:</span>
          <ol>
            <li>Студентам - 10%</li>
            <li>Группам от 5 человек - 7%</li>
            <li>При проживание более 5 дней - 7%</li>
            <li>При оплате единовременно за месяц - 20%</li>
            <li>Скидки не суммируются (исключение постоянным клиентам дополнительная скидка - 2%, со второго посещения).</li>
          </ol>
        </div>
      </div>
    </el-col>
  </el-row>
</template>

<style>
#about-row {
    padding: 40px 80px;
}

.ulist .list-title {
  font-weight: bold;
}

.ulist ul,
.ulist ol {
  list-style: none;
  margin-top: 0;
}
</style>