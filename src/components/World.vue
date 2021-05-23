<template>
  <div>
    <div class="title">МИР</div>
    <div class="header-methods-div">
      <div class="header-methods-buttons">
        <button v-for="(name, index) in methodsName"
                class="header-methods-button"
                :key="index"
                :id="'button-world-' + index"
                @click="selectMethod(index)">
          {{name}}
        </button>
      </div>
    </div>
    <div class="row">
      <div class="background-body1">
        <apexchart type="line"  :options="chartOptions" :series="series"></apexchart>
<!--        <img :src="images.graph" class="graph"/>-->
        <div class="legend">
          <div class="row1">
            <div class="line1-legend"></div>
            <div class="text-legend">Метод СИ - {{ activeText.title.toUpperCase()}}</div>
          </div>
          <div class="row1">
            <div class="line2-legend"></div>
            <div class="text-legend">ЦИФРОВИЗАЦИЯ</div>
          </div>
        </div>
      </div>
      <div class="background-body2">
        <div class="title-method">{{ activeText.title}}</div>
        <div class="text-container">
          <div class="line"></div>
          <div class="text-method">
            {{ activeText.text}}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "World",
  data() {
    return {
      images: {
        graph: require("@/assets/graph.png")
      },
      methodsName: ["Фишинг", "Троян-вымогатель", "Взлом деловой электронной почты", "Перехват данных электронной комерции",
        "Мошенническое ПО", "Кибер-мошенничество"],
      methodsText: [
        "text1",
        "text2",
        "text3",
        "text4",
        "text5",
        "text6"
      ],
      activeText: {
        title: "",
        text: "",
      },
      currentId: 0,

      series: [{
        name: "",
        data: [10, 41, 35, 51, 49, 62, 69, 91, 148],
        color: "#0FDBBB"
      },
        {
          name: "",
          data: [1, 2, 35, 51, 12, 62, 69, 2, 148],
          color: "#FC2847"
        }],

      chartOptions: {
        chart: {
          height: 350,
          type: 'line',
          zoom: {
            enabled: false
          },
          fontFamily: 'Jura, sans-serif',

        },
        dataLabels: {
          enabled: false
        },
        stroke: {
          curve: 'smooth'
        },
        title: {
          text: '',
          align: 'left'
        },
        grid: {
          show: false,
        },
        xaxis: {
          categories: ['1000', '1000', '1000', '1000', '1000', '1000', '1000', '1000', '1000'],
          axisTicks: {
            show: true
          },
          axisBorder: {
            show: true,
            color: "#FFFFFF"
          },
          labels: {
            style: {
              colors: "#FFFFFF"
            }
          },
          title: {
            text: "years",
            style: {
              color: "#FFFFFF",
              fontWeight: "noramal",
              fontSize: '16px',
            }
          }
        },
        yaxis: [
          {
            axisTicks: {
              show: true
            },
            axisBorder: {
              show: true,
              color: "#FFFFFF"
            },
            labels: {
              style: {
                colors: "#FFFFFF"
              }
            },
            title: {
              text: "%",
              style: {
                color: "#FFFFFF",
                fontWeight: "noramal",
                fontSize: '16px',
              }
            }
          }],
        legend: {
          show: false,
        }
      }
    }
  },

  methods: {

    selectMethod(id) {
      this.activeText.text = this.methodsText[id]
      this.activeText.title = this.methodsName[id]


      const button = document.getElementById("button-world-" + id)
      button.classList.remove("header-methods-button")
      button.classList.add("header-methods-button-active")

      const button1 = document.getElementById("button-world-" + this.currentId)
      button1.classList.remove("header-methods-button-active")
      button1.classList.add("header-methods-button")
      this.currentId = id;
    }
  },

  mounted() {
    if (this.methodsText.length > 0) {
      this.activeText.text = this.methodsText[0]
      this.activeText.title = this.methodsName[0]

      const button = document.getElementById("button-world-0")
      button.classList.remove("header-methods-button")
      button.classList.add("header-methods-button-active")
    } else {
      this.activeText.text = "Текст не найден"
      this.activeText.title = "Заголовок"
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
  background: rgba(62, 62, 62, 0.5);
  border-radius: 46px;
}

.header-methods-buttons {
  height: 100%;
  padding: 0 1em 0 1em;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.header-methods-button-active:focus, .header-methods-button-active:active {
  outline: none
}

.header-methods-button-active {
  background: rgba(36, 42, 48, 0.7);
  backdrop-filter: blur(3px);
  margin: 0 0.2em 0 0.2em;
  width: 100%;
  height: 70%;

  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;

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


.header-methods-button:focus, .header-methods-button:active {
  outline: none
}

.header-methods-button:hover {
  background: rgba(36, 42, 48, 0.7);
  backdrop-filter: blur(3px);
  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;
}

.header-methods-button-active {
  background: rgba(36, 42, 48, 0.7);
  backdrop-filter: blur(3px);
}


.header-methods-button {
  margin: 0 0.2em 0 0.2em;
  width: 100%;
  height: 70%;

  -webkit-transition: all 0.3s ease;;
  -moz-transition: all 0.3s ease;;
  -o-transition: all 0.3s ease;;
  transition: all 0.3s ease;

  background: rgba(36, 42, 48, 0);
  backdrop-filter: blur(3px);

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
  background: rgba(62, 62, 62, 0.5);
  backdrop-filter: blur(18px);
}

.background-body2 {
  width: 50%;
  margin: 0 2em 2em 2em;
  background: rgba(62, 62, 62, 0.5);
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