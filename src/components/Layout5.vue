<template>
  <div class="layout5">
    <div class="layout5_logo">
      <img class="layout5_logo_logo-cyberpunk" src="../assets/logo/Cyberpunk_2077_logo.png">
      <img class="layout5_logo_logo-cdproject" src="../assets/logo/cd-project_logo.png">
    </div>
    <div class="layout5_text">
      <span>Лицензия</span>
      <span>Политика конфиденциальности</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Layout5Component'
}
</script>

<style lang="scss">
.layout5 {
  box-sizing: border-box;
  background-color:  #ffffff;
  display: flex;
  justify-content: space-between;
  align-items: center;
  &_text {
    font-family: Roboto;
    font-size: 18px;
    font-weight: 400;
    line-height: 21px;
    letter-spacing: 0em;
    text-align: left;
    color: #000000;
  }
}
@media (min-width: 1920px)  {
  .layout5 {
    width: 1920px;
    padding: 13px 320px;
    height: 100px;
    &_logo {
      height: 74px;
      img {
        margin-right: 32px;
      }
    }
    &_text span{
        margin-right: 32px;
    }
  }
}
@media (min-width: 1024px) and (max-width: 1920px) {
  .layout5 {
    width: 1024px;
    padding: 13px 36px;
    height: 100px;
    &_logo {
      height: 74px;
      img {
        margin-right: 32px;
      }
    }
    &_text span {
      margin-right: 32px;
    }
  }
}
@media (min-width: 320px) and (max-width: 1024px){
  .layout5 {
    width: 320px;
    padding: 0px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    &_logo {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 190px;
      &_logo-cyberpunk {
        width: 200px;
        height: 50px;
        margin-bottom: 25px;
      }
      &_logo-cdproject {
        width: 116px;
        height: 50px;
      }
    }
    &_text { 
      width: 100%;
      height: 103px;
      font-size: 16px;
      font-weight: 400;
      line-height: 19px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background-color: #E6E6E6;
      span:first-child {
        margin-bottom: 15px;
      }
    }
  }
}
</style>