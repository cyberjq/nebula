<template>
  <div>
    <div class="select-country-div">
        ВЫБЕРИТЕ НЕОБХОДИМУЮ ОБЛАСТЬ ДЛЯ ПРОДОЛЖЕНИЯ
    </div>
    <div class="select-country-background">
        <div class="map-russian-div " @mouseover="mouseOverRussianMap" @mouseleave="mouseLeaveRussianMap" >
          <img :src="russianMap" v-if="isRussianMap" class="map-russian" v-on:click="moveRussia">
        </div>
      <img :src="currentMap" @mouseover="mouseOverCurrentMap" @mouseleave="mouseLeaveCurrentMap" class="map-img"
           v-on:click="moveWorld"/>

        <div class="content">
          <!--Россия -->
          <div >
            <div class="title">Российская Федерация</div>
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
        map: require("@/assets/map.svg"),
        worldMap: require("@/assets/world-map.svg"),
        russianMap: require("@/assets/russian-map.svg")
      },
      currentMap: "",
      russianMap: "",
      isRussianMap: false,

      classObject: {
        active: false,
        position: "absolute"
      }
    }
  },

  methods: {
    mouseOverCurrentMap() {
      this.currentMap = this.images.worldMap;
      const title = document.getElementsByClassName("title-other")[0]
      title.classList.add("shadow")
    },

    mouseLeaveCurrentMap() {
      this.currentMap = this.images.map;
      const title = document.getElementsByClassName("title-other")[0]
      title.classList.remove("shadow")
    },

    mouseOverRussianMap(){
      this.isRussianMap = true
      const title = document.getElementsByClassName("title")[0]
      title.classList.add("shadow")
    },

    mouseLeaveRussianMap() {
      this.isRussianMap = false
      const title = document.getElementsByClassName("title")[0]
      title.classList.remove("shadow")
    },

    moveWorld() {
      window.scrollTo({top: 5980, behavior: 'smooth'});
    },

    moveRussia() {
      window.scrollTo({top: 4900, behavior: 'smooth'});
    }
  },

  mounted() {
    this.currentMap = this.images.map;
    this.russianMap = this.images.russianMap;
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
  margin: 6em 6em 6em 6em;

}

.map-russian:hover {
  visibility: visible;
}

.map-russian-div {
  position: absolute;
  width: 600px;
  height: 380.9125px;
  top: 98px;
  left: 680px
}

.map-russian {
  position: absolute;
  width: 100%;
  height: 100%;
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

.shadow {

  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;
  text-shadow: 0px 0px 15px white;
}

.title {

  margin: 0 0 1.5em 0;
  font-style: normal;
  font-weight: bold;
  font-size: 36px;
  line-height: 116.3%;
  /* or 42px */

  text-align: right;
  letter-spacing: 0.1em;

  color: #FFFFFF;

  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;

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

  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;
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