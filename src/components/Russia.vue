<template>
  <div>
    <div class="title">РОССИЙСКАЯ ФЕДЕРАЦИЯ</div>
    <div class="header-methods-div">
      <div class="header-methods-buttons">
        <button class="header-methods-button">Фишинг</button>
        <button class="header-methods-button">Троян-вымогатель</button>
        <button class="header-methods-button">Взлом деловой электронной почты</button>
        <button class="header-methods-button">Перехват данных электронной коммерции</button>
        <button class="header-methods-button">Мошенническое ПО</button>
        <button class="header-methods-button">Кибер-мошенничество</button>
      </div>
    </div>
    <div class="row">
      <div class="background-body1">
        <img :src="images.graph" class="graph"/>
        <div class="legend">
          <div class="row1">
            <div class="line1-legend"></div>
            <div class="text-legend">Метод СИ - ФИШИНГ</div>
          </div>
          <div class="row1">
            <div class="line2-legend"></div>
            <div class="text-legend">ЦИФРОВИЗАЦИЯ</div>
          </div>
        </div>
      </div>
      <div class="background-body2">
        <div class="title-method">Фишинг</div>
        <div class="text-container">
          <div class="line"></div>
          <div class="text-method">
            Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль
            в формировании форм воздействия. Значимость этих проблем настолько очевидна, что постоянное
            информационно-техническое обеспечение нашей деятельности в значительной степени обуславливает создание
            позиций, занимаемых участниками в отношении поставленных задач? Дорогие друзья, курс на
            социально-ориентированный национальный проект в значительной степени обуславливает создание дальнейших
            направлений развития проекта. Разнообразный и богатый опыт сложившаяся структура организации обеспечивает
            актуальность новых предложений!Значимость этих проблем настолько очевидна, что сложившаяся структура
            организации играет важную роль в формировании форм воздействия. Значимость этих проблем настолько очевидна,
            что сложившаяся структура организации играет важную роль в формировании форм воздействия.
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Russia",

  data() {
    return {
      images: {
        graph: require("@/assets/graph.png")
      }
    }
  }
}
</script>

<style scoped>

.title {

  margin: 1em 0 0 0;
  display: flex;

  width: 100%;
  height: 61px;

  justify-content: center;

  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  line-height: 116.3%;
  /* or 52px */
  letter-spacing: 0.1em;
  color: #242A30;
}

.header-methods-div {
  margin: 1em 3em 4em 3em;
  height: 94px;
  background: rgba(62, 62, 62, 0.3);
  border-radius: 46px;
}

.header-methods-buttons {
  height: 100%;
  padding: 0 1em 0 1em;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.header-methods-button {
  /*width: 290px;*/
  margin: 0 0.2em 0 0.2em;
  width: 100%;
  height: 70%;

  background: rgba(61, 61, 61, 0.36);
  backdrop-filter: blur(3px);
  border-radius: 46px;
  border: 0;
  font-family: Jura,sans-serif;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  letter-spacing: 0.05em;
  color: #FFFFFF;
}

.row {
  flex-direction: row;
  display: flex;
  margin: 0 5em 0 5em;
}

.row1 {
  flex-direction: row;
  display: flex;
  align-items: center;
}

.background-body1 {
  width: 50%;
  margin: 0 4em 2em 2em;
  background: rgba(62, 62, 62, 0.4);
  backdrop-filter: blur(18px);
}

.background-body2 {
  width: 50%;
  margin: 0 2em 2em 2em;
  background: rgba(62, 62, 62, 0.4);
  backdrop-filter: blur(18px);
}

.graph {
  margin: 2em 2em 0 2em;
}

.title-method {
  margin: 2em 0 1em 0;
  font-style: normal;
  font-size: 34px;
  line-height: 116.3%;
  letter-spacing: 0.1em;
  text-align: center;
  color: #FFFFFF;
}


.line {
  margin: 0 0 2em 0;
  color: #0FDBBB;
  border: 2px solid #0FDBBB;
  box-shadow: 0px 0px 10px #0FDBBB;
}

.text-method {

  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  text-align: center;
  letter-spacing: 0.1em;

  color: #FFFFFF;
}

.legend {
  margin: 1.5em;
  padding: 1.5em;
  background: rgba(36, 42, 48, 0.6);
  border-radius: 25px;
}

.text-legend {
  margin: 0 2em 0.5em 2em;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  letter-spacing: 0.1em;

  color: #FFFFFF;
}

.line1-legend {
  width: 25%;
  height: 0px;
  border: 2px solid #0FDBBB;
  box-shadow: 0px 0px 10px #0FDBBB;
}

.line2-legend {
  width: 25%;
  height: 0px;
  border: 2px solid #FC2847;
  box-shadow: 0px 0px 10px #FC2847;
}

.text-container {
  margin: 0 4em 0 4em;
}


</style>