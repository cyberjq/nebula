<template>
  <div class="container">
    <div class="title">МЕТОДЫ ЗАЩИТЫ</div>
    <div class="row">
      <div class="card card1">
        <div class="card-title">{{methodsName[0]}}</div>
        <div class="card-text">
          {{methodsText[0]}}
        </div>
      </div>

      <div class="card card2">
        <div class="card-title">{{methodsName[1]}}</div>
        <div class="card-text">
          {{methodsText[1]}}
        </div>
      </div>


      <div class="card">
        <div class="card-title">{{methodsName[2]}}</div>
        <div class="card-text">
          {{methodsText[2]}}
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: "MethodsOfProtection",

  data() {
    return {
      methodsName: ["Метод1", "Метод2", "Метод3"],
      methodsText: [" Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль\n" +
      "          в формировании форм воздействия. Значимость этих проблем настолько очевидна, что постоянное\n" +
      "          информационно-техническое обеспечение нашей деятельности в значительной степени обуславливает\n" +
      "          создание позиций.", " Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль\n" +
      "          в формировании форм воздействия. Значимость этих проблем настолько очевидна, что постоянное\n" +
      "          информационно-техническое обеспечение нашей деятельности в значительной степени обуславливает\n" +
      "          создание позиций.", " Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль\n" +
      "          в формировании форм воздействия. Значимость этих проблем настолько очевидна, что постоянное\n" +
      "          информационно-техническое обеспечение нашей деятельности в значительной степени обуславливает\n" +
      "          создание позиций."]
    }
  }
}
</script>

<style scoped>

.container {
  display: flex;
  flex-direction: column;
}

.title {

  margin: 6.2em 0 0 0;

  text-align: center;
  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  letter-spacing: 0.25em;
  color: #FFFFFF;
}

.row {
  margin: 8em 12em 0 12em;
  display: flex;
  flex-direction: row;
}

.card {
  background: rgba(196, 196, 196, 0.2);
  display: table;
  width: 30%;
}

.card2 {
  margin: 12em 7em 0 7em;
}

.card1 {
  margin: 6em 0 0 0;
}


.card-title {
  margin: 1.5em;
  font-weight: bold;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  text-align: center;
  letter-spacing: 0.1em;

  color: #242A30;
}

.card-text {
  margin: 1.5em;
  font-style: normal;
  font-weight: 500;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  text-align: center;
  letter-spacing: 0.1em;

  color: #242A30;
}


</style>