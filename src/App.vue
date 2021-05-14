<template>
    <Greeting class="greeting"/>
</template>

<script>
import Greeting from './components/Greeting.vue'


export default {
  name: 'App',
  components: {
    Greeting
  }
}
</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Jura&display=swap');

body {

  font-family: 'Jura', sans-serif;

  margin: 0;
  padding: 0;
  display: grid;
}

.greeting {
  background: #ffffff url("assets/greeting_background.svg");
  width: 100%;
  height: 1080px;
}

</style>
