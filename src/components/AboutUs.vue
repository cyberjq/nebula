<template>
  <div>
    <div class="container">
      <div class="about-us-div">
          <div class="about-us-p">
            О НАС
          </div>
      </div>
      <div>
        <div class="body-about-us-div">
          <div class="body-about-div">
            <div class="header-about-div-and-text">Кто мы</div>
            <div class="separator"></div>
            <div class="body-about-text">
              Мы студенты МГТУ им. Н. Э. Баумана. Нам показалось интересным выявить какие-либо закономерности между
              методами социальной инженерии и увеличением аудитории Интернета как в России, так и во всем мире.
            </div>

          </div>
          <div class="body-about-div">
            <div class="header-about-div-and-text">Зачем мы</div>
            <div class="separator"></div>
            <div class="body-about-text">
              Наша цель - не только показать тенденции социальной инженерии
              в условиях цифровизации общества, но и предоставить инструментарий,
              который поможет снизить или даже предотвратить попытку «взлома» человека.
            </div>

          </div>
          <div class="body-about-div">
            <div class="header-about-div-and-text">Можно ли нам доверять?</div>
            <div class="separator"></div>
            <div class="body-about-text">
              Нашими источниками являются такие сайты, как SecureList
              от <a href="https://securelist.ru/"> Лаборатории Касперского</a>,
              <a href="http://www.antiphishing.org/trendsreports/">APWG</a>, специализирующиеся на фишинге,
              <a href="https://purplesec.us/resources/cyber-security-statistics/">Purplesec</a>,
              <a href="https://www.pandasecurity.com/">PandaLab</a>, специализирующаяся на компьютерной безопасности
            </div>
          </div>
        </div>
      </div>
      <div class="detail-si-text">ПОДРОБНЕЕ О МЕТОДАХ СОЦИАЛЬНОЙ ИНЖЕНЕРИИ</div>
      <div class="arrows-div"><img :src="images.arrows" class="arrows-img"/></div>
      <div class="header-methods-div">
        <div class="header-methods-buttons">
          <button v-for="(name, index) in methodsName"
                  class="header-methods-button"
                  :key="index"
                  :id="'button-' + index"
                  @click="selectMethod(index)">
            {{name}}
          </button>
        </div>

      </div>
      <div class="method-div">
        <div class="method-text" id="text">{{activeText}}</div>

      </div>
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
      },
      methodsName: ["Фишинг", "Троян-вымогатель", "ВПО"],
      methodsText: [
       "Фишингом (англ. phishing от fishing – «рыбная ловля», «выуживание») называют получение информации " +
       "в Интернет-пространстве за счёт невнимательности жертвы. Данный метод является одним из самых популярных " +
       "в социальной инженерии. Обычно он представляет собой массовые рассылки спама по электронной почте. " +
       "Потенциальным жертвам приходят письма якобы от сервисов, которыми они пользуются: платежных систем, " +
       "онлайн-магазинов и т.п. Чтобы вызвать больше доверия, мошенники придумывают серьезные причины для перехода" +
       " по ссылке: например, просят жертву обновить пароль или подтвердить какое-то действие в системе. " +
       "Несмотря на распространенность данного метода социальной инженерии, многие, тем не менее, " +
       "попадаются на его «удочку».",
        "text3",
          "Внедрение вредоносного ПО в настоящее время активно применяется в социальных сетях путём взлома электронной " +
          "почты или учётной записи пользователя. Таким образом злоумышленник получает доступ к контактам жертвы, " +
          "чтобы потом от её имени разослать ссылку на вредоносное ПО.\n Ввиду ситуации " +
          "с коронавирусом произошло усложнение фишинговых схем. В этих условиях специалистами, " +
          "занимающимися анализом современных киберпреступлений, было введено новое определение " +
          "для описания данных видов кибератак – «социально спроектированное вредоносное ПО», " +
          "которое злоумышленники стали чаще использовать для повышения шансов заражения компьютеров пользователей." +
          " Привлекая внимание потенциальной жертвы фишинговыми методами, они повышают вероятность" +
          " проникновения вредоносного объекта в компьютер пользователя. Другими словами, фишинг стал " +
          "проводником вредоносных ПО. В ходе использования нового метода мы можем увидеть более изощрённое" +
          " манипулирование сознанием обычных пользователей Интернета, которые начинают доверять хакерам и " +
          "предоставляют им необходимую информацию.\n",
          "text4",
          "text5",
        "text6"
      ],
      activeText: "",
      currentId: 0,
    }
  },

  methods: {

    selectMethod(id) {
       this.activeText = this.methodsText[id];

        const button = document.getElementById("button-" + id)
        button.classList.remove("header-methods-button")
        button.classList.add("header-methods-button-active")

        const button1 = document.getElementById("button-" + this.currentId)
        button1.classList.remove("header-methods-button-active")
        button1.classList.add("header-methods-button")
        this.currentId = id;
    }
  },

  mounted() {
    if (this.methodsText.length > 0) {
      this.activeText = this.methodsText[0]
      const button = document.getElementById("button-0")
      button.classList.remove("header-methods-button")
      button.classList.add("header-methods-button-active")

    } else {
      this.activeText = "Текст не найден"
    }
  }
}
</script>

<style scoped>

.container {
  display: flex;
  flex-direction: column;
}


a:visited {
  color: #242A30;
}

a {
  color: #F73C57;
}

.about-us-div {

  /*height: 100px;*/
  /*width: 20%;*/
  /*left: 40%;*/
  /*!*left: 713px;*!*/
  /*!*width: 495px;*!*/
  /*top: 73px;*/

  text-align: center;
  margin: 1em 17em 0 17em;
  padding: 0.2em;

  background: #242A30;
  opacity: 0.7;
  box-shadow: 0px 0px 17px #242A30;
  border-radius: 2px;

  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  line-height: 116.3%;
  letter-spacing: 0.1em;
  color: #ffffff;
  justify-content: center;
  align-items: center;
}


.header-about-div-and-text {
  margin: 1em 0 1em 0;
  display: flex;
  font-style: normal;
  font-weight: bold;
  font-size: 24px;
  line-height: 116.3%;

  letter-spacing: 0.1em;
  align-items: center;
  justify-content: center;
  text-align: center;
  color: #000000;
  border-radius: 11px;
}

.separator {
  border: 2px solid #0FDBBB;
  box-shadow: 0px 0px 10px #0FDBBB;
  margin: 0 1.5em 0 1.5em;
}

.body-about-us-div {
  /*height: 287px;*/
  margin: 8em 2em 0 2em;
  display: flex;
  justify-content: space-around;
}

.body-about-div {
  display: flex;
  flex-direction: column;
  width: 25%;
  background: linear-gradient(180deg, rgba(236, 236, 236, 0.9) 90%, rgba(236, 236, 236, 0.17) 100%);
  box-shadow: 0px 0px 68px 11px rgba(0, 0, 0, 0.4);
}

.body-about-text {
  align-items: center;
  margin: 1.5em;
  font-style: normal;
  font-weight: bold;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */

  text-align: center;
  letter-spacing: 0.1em;

  color: #242A30;
}


.detail-si-text {
  /*position: absolute;*/
  width: 100%;
  height: 52px;

  margin: 3em 0 0.5em 0 ;

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
  /*position: absolute;*/
  display: flex;
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
  /*position: absolute;*/

  height: 100px;
  top: 866px;
  margin: 0 9em 0 9em;
  background: rgba(236, 236, 236, 0.03);
  backdrop-filter: blur(5px);
}

.header-methods-buttons {
  height: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}


.header-methods-button:focus, .header-methods-button:active {
  outline: none
}

.header-methods-button:hover {
  border-bottom: 4px solid #F73C57;
  /*box-shadow: 0 4px 2px -2px #F73C57;*/
}

.header-methods-button-active:focus, .header-methods-button-active:active {
  border-bottom: 4px solid #F73C57;
  /*box-shadow: 0 4px 2px -2px #F73C57;*/
}


.header-methods-button-active {

  width: 100%;
  height: 80%;
  font-family: Jura,sans-serif;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */
  letter-spacing: 0.05em;
  background: rgba(255, 255, 255, 0);
  border: 0;
  border-bottom: 4px solid #F73C57;
  color: #FFF;
  text-shadow: 0px 0px 15px #ECECEC;
}


.header-methods-button {
  width: 100%;
  height: 80%;

  font-family: Jura,sans-serif;
  font-style: normal;
  font-size: 20px;
  line-height: 116.3%;
  /* or 23px */
  letter-spacing: 0.05em;

  background: rgba(255, 255, 255, 0);
  border: 0;
  color: #FFF;
}

.method-div {
  /* Rectangle 75 */

  /*position: absolute;*/
  /*width: 80%;*/
  /*height: 496px;*/
  /*left: 10%;*/
  /*top: 1018px;*/
  margin: 0 9em 0 9em;
  background: rgba(236, 236, 236, 0.03);
  backdrop-filter: blur(5px);
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