<template>
  <div>
    <div class="title-russia">РОССИЙСКАЯ ФЕДЕРАЦИЯ</div>
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
    <div class="body-russia">
      <div class="background-body">F</div>
      <div class="background-body">A</div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Russia"
}
</script>

<style scoped>

.title-russia {

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
  margin: 1em 6em 0 6em;
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
  margin: 0 0.5em 0 0.5em;
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

.body-russia {
  width: 100%;
  height: 100%;
  flex-direction: row;
  display: flex;
  margin: 2em;
}

.background-body {
  width: 100px;
  background: rgba(62, 62, 62, 0.4);
  backdrop-filter: blur(18px);
}

</style>