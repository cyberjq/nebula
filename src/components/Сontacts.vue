<template>
  <div>
    <div class="container">
      <div class="background">
        <div class="text">
          КОНТАКТЫ
        </div>
      </div>
      <div  class="background background1 row">
        <div class="text">
          E-mail:
        </div>
        <div class="col">
          <div class="text">
            maksimovaea@student.bmstu.ru
          </div>
          <div class="text text1">
            opletinapv@student.bmstu.ru
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<script>
export default {
  name: "Сontacts"
}
</script>

<style scoped>

.container {
  position: absolute;
  top: 46%;
  left: 39%;
  display: flex;
  flex-direction: column;
}

.row {
  display: flex;
  flex-direction: row;
}

.col {
  margin: 0 0 0 2em;
  display: flex;
  flex-direction: column;
}

.background {
  padding: 1em;
  background: rgba(111, 113, 116, 0.45);
  backdrop-filter: blur(10px);
  /* Note: backdrop-filter has minimal browser support */

  border-radius: 7px;
}

.background1 {
  margin: 2em 0 0 0;
}

.text {
  font-style: normal;
  font-size: 20px;
  /* or 74px */
  display: flex;
  align-items: center;
  color: #FFFFFF;
}

.text1 {
  margin: 1em 0 0 0;
}

</style>