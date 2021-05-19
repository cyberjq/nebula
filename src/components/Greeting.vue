<template>
  <div class="container">
    <div>
      <h3 class="greeting-text">Исследуй социальную инженерию вместе с N.E.B.U.L.O.</h3>
    </div>
    <div>
      <h1 class="project-text">N.E.B.U.L.O.</h1>
    </div>
    <div>
      <button class="greeting-button">НАЧАТЬ</button>
      <img :src="images.hacker" class="greeting-hacker"/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Greeting',
  props: {
    msg: String
  },

  data() {
    return {
      images: {
        hacker: require("@/assets/hacker.png"),
        background: require("@/assets/greeting_background.svg")
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.project-text {
  position: absolute;
  width: 987px;
  height: 228px;
  left: 165px;
  top: 335px;

  font-style: normal;
  font-weight: bold;
  font-size: 120px;


  letter-spacing: 0.08em;

  color: #31475B;

  text-shadow: 0px 0px 84px rgba(49, 71, 91, 0.45);
}

.greeting-button:active, button:focus {
  outline: none
}

.greeting-button{
  position: absolute;
  width: 511px;
  height: 104px;
  left: 177px;
  top: 726px;

  background: #0FDBBB;
  /* Drop shadow */

  box-shadow: 0px 0px 20px rgba(15, 219, 187, 0.7);
  border-radius: 11px;
  border: 0;

  font-family: 'Jura', sans-serif;
  font-style: normal;
  font-weight: bold;
  font-size: 50px;
  line-height: 116.3%;
  /* or 58px */

  letter-spacing: 0.05em;

  color: #FFFFFF;
}

.greeting-text {
  position: absolute;
  left: 23%;
  right: 38%;
  top: 2.5%;
  bottom: 97.08%;

  font-style: normal;
  font-weight: bold;
  font-size: 45px;
  line-height: 156.8%;
  /* or 71px */

  text-align: right;
  letter-spacing: 0.24em;

  color: #31475B;
}

.greeting-hacker {
  position: absolute;
  width: 792px;
  height: 798px;
  left: 1051px;
  top: 305px;
}

</style>
