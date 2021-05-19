<template>
  <div>
      <Greeting class="greeting"/>
      <SocialEngineering class="social-engineering"/>
      <AboutUs class="about-us"></AboutUs>
      <Country class="country"></Country>
      <Russia class="russia"></Russia>
  </div>

</template>

<script>
import Greeting from './components/Greeting.vue'
import SocialEngineering from './components/SocialEngineering'
import AboutUs from "@/components/AboutUs";
import Country from "@/components/Country";
import Russia from "@/components/Russia";

export default {
  name: 'App',
  components: {
    Greeting,
    SocialEngineering,
    AboutUs,
    Country,
    Russia
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
  background-size: cover;
  width: 100%;
  height: 1080px;
}


.social-engineering {
  position: absolute;
  width: 100%;
  height: 1082px;
  top: 1079px;
  backdrop-filter: blur(12px);
  background: rgba(36, 42, 48, 0.8) url("assets/si-background.svg") center;
  background-size: cover;
}

.about-us {
  position: absolute;
  width: 100%;
  height: 2304px;
  top: 2160px;
  background: #ffffff url("assets/about-us.svg");
  background-size: cover;
  background-position-y: -107px;

}

.country {
  position: absolute;
  width: 100%;
  top: 3720px;
}

.russia {
  position: absolute;
  width: 100%;
  /*height: 100%;*/
  height: 1080px;
  top: 4900px;
  background: #ffffff url("assets/russia-background.svg");
  background-size: cover;
  /*background-position-y: -107px;*/
}

</style>
