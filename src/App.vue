<template>
  <div id="app">
    <div class="app_container">
      <layout></layout>
      <layout1></layout1>
      <layout2></layout2>
      <layout3></layout3>
      <layout4></layout4>
      <layout5></layout5>
      <layout6></layout6>
    </div>
  </div>
</template> 

<script>
import Layout from './components/Layout.vue'
import Layout1 from './components/Layout1.vue'
import Layout2 from './components/Layout2.vue'
import Layout3 from './components/Layout3.vue'
import Layout4 from './components/Layout4.vue'
import Layout5 from './components/Layout5.vue'
import Layout6 from './components/Layout6.vue'

export default {
  name: 'App',
  components: {
    Layout, Layout1, Layout2, Layout3, Layout4, Layout5, Layout6
  }
}
</script>

<style lang="scss">
#app {
  display: flex;
  justify-content: center;
  width: 100%;
  box-sizing: border-box;
}
.app_container {
  display: flex;
  justify-content: center;
  flex-direction: column;
}
.header-font {
  font-family: Archangelsk;
  line-height: 63.3px;
  letter-spacing: 0em;
  text-align: left;
  font-size: 62px;
  font-weight: 400;
}
.color-black {
  color: #000000;
}
.color-white {
  color: #ffffff;
}
.color-gray {
color: #777777;
}
.game-description {
  font-family: Roboto;
  font-weight: 400;
  font-size: 18px;
  line-height: 34px;
  &_title {
    font-family: Roboto;
    font-size: 18px;
    font-weight: 700;
    line-height: 34px;
    letter-spacing: 0em;
    text-align: left;
    color: #52BEDC;
  }
}
button {
  cursor: pointer;
}
@media (min-width: 1920px)  {
  .app_container {
    width: 1920px;
  }
}
@media (min-width: 1024px) and (max-width: 1920px) {
  .app_container {
    width: 1024px;
  }    
}
@media (min-width: 320px) and (max-width: 1024px){
  .app_container {
    width: 320px;
  } 
  .header-font {
    font-size: 30px;
    font-weight: 400;
    line-height: 31px;
  }
  .game-description {
    padding: 0px 12px;
    font-size: 16px;
    font-weight: 400;
    line-height: 32px;
    &-title {
      font-size: 16px;
      font-weight: 700;
      line-height: 32px;
    }
  }   
}
@font-face {
  font-family: "Archangelsk";
  src: url("./assets/font/ofont.ru_Archangelsk.ttf");
}
@font-face {
  font-family: "Roboto";
  src: url("./assets/font/ofont.ru_Roboto.ttf");
}    
</style>