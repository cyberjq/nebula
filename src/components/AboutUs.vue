<template>
  <div>
    <div class="about-us-div"><div class="about-us-background-div"><div class="about-us-p">О НАС</div></div></div>
    <div>

      <div class="header-about-us-div">
        <div class="header-about-div-and-text">Кто мы</div>
        <div class="header-about-div-and-text">Зачем мы</div>
        <div class="header-about-div-and-text">Можно ли нам доверять?</div>
      </div>

      <div class="body-about-us-div">
        <div class="body-about-div">
          <div class="body-about-text">
            Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль в
          формировании форм воздействия.
          </div>

        </div>
        <div class="body-about-div">
          <div class="body-about-text">
            Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль в
            формировании форм воздействия.
          </div>

        </div>
        <div class="body-about-div">
          <div class="body-about-text">
            Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль в
            формировании форм воздействия.
          </div>

        </div>
      </div>
    </div>
    <div class="detail-si-text">ПОДРОБНЕЕ О МЕТОДАХ СОЦИАЛЬНОЙ ИНЖЕНЕРИИ</div>
    <div class="arrows-div"><img :src="images.arrows" class="arrows-img"/></div>
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
    <div class="method-div">
      <div class="method-text">  Значимость этих проблем настолько очевидна, что сложившаяся структура организации играет важную роль в
        формировании форм воздействия. Значимость этих проблем настолько очевидна, что постоянное информационно-техническое
        обеспечение нашей деятельности в значительной степени обуславливает создание позиций, занимаемых участниками
        в отношении поставленных задач? Дорогие друзья, курс на социально-ориентированный национальный проект
        в значительной степени обуславливает создание дальнейших направлений развития проекта. Разнообразный и
        богатый опыт сложившаяся структура организации обеспечивает актуальность новых предложений! Повседневная
        практика показывает, что выбранный нами инновационный путь напрямую зависит от новых предложений. Дорогие
        друзья, курс на социально-ориентированный национальный проект в значительной степени обуславливает создание
        дальнейших направлений развития проекта. Разнообразный и богатый опыт сложившаяся структура организации
        обеспечивает актуальность новых предложений! Повседневная практика показывает, что выбранный нами инновационный
        путь напрямую зависит от новых предложений.</div>

    </div>
  </div>
</template>

<script>
export default {
  name: "AboutUs",

  data() {
    return {
      images: {
        arrows: require("@/assets/arrows.png")
      }
    }
  }
}
</script>

<style scoped>

.about-us-div {

  position: absolute;

  height: 100px;
  width: 20%;
  left: 40%;
  /*left: 713px;*/
  /*width: 495px;*/
  top: 73px;

  background: rgba(196, 196, 196, 0.25);
  backdrop-filter: blur(6px);
  /* Note: backdrop-filter has minimal browser support */

  border-radius: 22px;

  font-style: normal;
  font-weight: bold;
  font-size: 55px;
  line-height: 116.3%;
  /* identical to box height, or 64px */

  letter-spacing: 0.1em;

  color: #000000;
}



.about-us-p {
  position: absolute;
  width: 100%;
  height: 100%;
  display: flex;
  /* О НАС */
  font-style: normal;
  font-weight: bold;
  font-size: 55px;
  line-height: 116.3%;
  letter-spacing: 0.1em;
  color: #000000;
  justify-content: center;
  align-items: center;
}


.header-about-us-div {
  position: absolute;
  height: 60px;
  width: 80%;
  left: 10%;
  right: 10%;
  top: 286px;
  display: flex;
  justify-content: space-around;
}

.header-about-div-and-text {
  display: flex;
  width: 325px;
  height: 100%;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 116.3%;
  /* or 28px */
  letter-spacing: 0.1em;
  align-items: center;
  justify-content: center;
  text-align: center;

  color: #000000;
  background: #C4C4C4;
  border-radius: 11px;

}

.body-about-us-div {
  position: absolute;
  height: 287px;
  width: 80%;
  left: 10%;
  right: 10%;
  top: 357px;
  display: flex;
  justify-content: space-around;
}

.body-about-div {
  display: flex;
  width: 325px;
  height: 100%;

  background: #C4C4C4;
  border-radius: 20px 20px 0 0;
}

.body-about-text {
  align-items: center;
  margin: 1.5em;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  letter-spacing: 0.1em;
  color: #FFFFFF;
}


.detail-si-text {
  position: absolute;
  width: 100%;
  height: 52px;
  top: 701px;
  text-align: center;

  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  line-height: 116.3%;
  /* or 52px */

  letter-spacing: 0.02em;

  color: #E9E9E9;
}

.arrows-div {
  position: absolute;
  display: flex;
  top: 777px;
  width: 100%;
  justify-content: center;
}

.arrows-img {
  width: 90px;
  height: 90px;
  opacity: 0.7;
  filter: drop-shadow(0px 0px 23px rgba(247, 60, 87, 0.9));
}

.header-methods-div {
  position: absolute;
  width: 90%;
  height: 94px;
  left: 5%;
  top: 866px;
  background: rgba(186, 186, 186, 0.45);
  border-radius: 46px;
}

.header-methods-buttons {
  height: 94px;
  padding: 0 1em 0 1em;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.header-methods-button {
  width: 290px;
  height: 67px;

  background: rgba(36, 42, 48, 0.7);
  backdrop-filter: blur(3px);
  /* Note: backdrop-filter has minimal browser support */

  border-radius: 46px;
  border: 0;

  font-family: Jura,sans-serif;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  letter-spacing: 0.05em;

  color: #FFFFFF;
}

.method-div {
  /* Rectangle 75 */

  position: absolute;
  width: 80%;
  height: 496px;
  left: 10%;
  top: 1018px;

  background: rgba(236, 236, 236, 0.03);
  backdrop-filter: blur(9px);
}

.method-text {
  padding: 0 5em 0 5em;
  height: 496px;
  display: flex;
  align-items: center;
  font-style: normal;
  font-size: 24px;
  line-height: 116.3%;
  /* or 23px */

  text-align: center;
  letter-spacing: 0.1em;

  color: #FFFFFF;
}

</style>