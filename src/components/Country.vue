<template>
  <div>
    <div class="select-country-div">
        ВЫБЕРИТЕ НЕОБХОДИМУЮ ОБЛАСТЬ ДЛЯ ПРОДОЛЖЕНИЯ
    </div>
    <div class="select-country-background">
        <img :src="images.map" class="map-img"/>
        <div class="content">
          <!--Россия -->
          <div >
            <div class="title-russia">Российская Федерация</div>
            <div class="row">
              <div class="border-left-div"></div>
              <div class="text">
                Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную
                роль. Дорогие друзья, курс на социально-ориентированный национальный
              </div>
            </div>
          </div>
          <!--США -->
          <div>
            <div class="title-other">Мир</div>
            <div class="row">
              <div class="text">
                Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную
                роль. Дорогие друзья, курс на социально-ориентированный национальный
              </div>
              <div class="border-right-div"></div>
            </div>
          </div>
        </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "Country",

  data() {
    return {
      images: {
        map: require("@/assets/map.png")
      }
    }
  }
}
</script>

<style scoped>

.select-country-div {
  position: absolute;
  width: 100%;
  height: 165px;
  background: #0FDBBB;
  display: flex;
  align-items: center;
  justify-content: center;

  font-style: normal;
  font-weight: bold;
  font-size: 40px;
  line-height: 116.3%;
  /* or 47px */
  letter-spacing: 0.055em;
  color: #242A30;
}

.select-country-background {
  position: absolute;
  display: flex;
  width: 100%;
  height: 1023px;
  top: 165px;
  background: #242A30;
  box-shadow: 10px 0px 30px rgba(0, 0, 0, 0.6);
}

.map-img {
  width: 100%;
  height: 90%;
  top: 50px;
}

.border-left-div {
  width: 2px;

  margin: 0 2.5em 0 0;
  background: #FC2847;
  box-shadow: 0px 0px 5px #FC2847;
}

.border-right-div {
  width: 2px;

  margin: 0 0 0 2.5em;
  background: #FC2847;
  box-shadow: 0px 0px 5px #FC2847;
}

.col {
  flex-direction: column;
}

.row {
  display: flex;
  flex-direction: row;
}

.title-russia {

  margin: 0 0 1.5em 0;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 116.3%;
  /* or 42px */

  text-align: right;
  letter-spacing: 0.1em;

  color: #FFFFFF;
}

.title-other {
  margin: 1.5em 0 1.5em 0;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 116.3%;
  /* or 42px */

  letter-spacing: 0.1em;

  color: #FFFFFF;
}

.text {
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  letter-spacing: 0.1em;

  color: #FFFFFF;
}

.content {
  padding: 8em 10em 0 0;
}

</style>