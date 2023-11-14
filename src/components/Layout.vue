<template>
    <div class="layout">
      <div class="layout_container">
      <div class="layout_container_header container-header">
        <div><img class="container-header_сyberpunk-logo" src="../assets/logo/Cyberpunk_2077_logo.png"></div>
        <div class="container-header_logo">
          <img src="../assets/logo/youtube_logo.png">
          <img src="../assets/logo/vkontakte_logo.png">
          <img src="../assets/logo/facebook_logo.png">
          <img src="../assets/logo/twitter_logo.png">
          <img src="../assets/logo/twitch_logo.png">
          <img src="../assets/logo/instagram_logo.png">
        </div>
      </div>
      <div class="layout_container_banner container-banner">
        <span class="container-banner_text header-font color-black">Доступно на всех платформах</span>
        <button class="container-banner_btn">Узнать больше</button>
      </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'LayoutComponent',
}
</script>

<style scoped lang="scss">
@keyframes changebackground {
  from {
    background-image: url("../assets/background.jpg");
  }
  30% {
    background-image: url("../assets/background2.jpg");
  }
  70% {
    background-image: url("../assets/background3.jpg");
  }
  to {
    background-image: url("../assets/background.jpg");
  }
}
@keyframes changebackground1024 {
  from {
    background-image: url("../assets/background_1024.jpg");
  }
  30% {
    background-image: url("../assets/background2_1024.jpg");
  }
  70% {
    background-image: url("../assets/background3_1024.jpg");
  }
  to {
    background-image: url("../assets/background_1024.jpg");
  }
}
.layout {
  //background-image: url("../assets/background.jpg");
  background-position: 50% 50%;
  width: 100%;
  height: 1000px;
  background-size: cover;
  animation: changebackground 20s infinite;
  
  
  &_container {
    display: flex;
    align-items: flex-end;
    flex-direction: column;
    justify-content: space-between;
    height: 100%;
    padding: 0px 320px;
    .container-header {
      margin-top: 20px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      &_сyberpunk-logo {
        width: 296px;
        height: 74px;
      }
      &_logo {
        width: 379px;
        height: 30px;
        display: flex;
        justify-content: space-between;
        img {
          width: 30px;
          height: 30px;
        }
      }
    }
    .container-banner {
      width: 624px;
      height: 369px;
      padding: 70px;
      box-sizing: border-box;
      display: flex;
      align-items: flex-start;
      flex-direction: column;
      justify-content: space-between;
      background-color: #F8F200;
      clip-path: polygon(10% 0, 100% 0, 100% 20%, 100% 90%, 90% 100%, 0 100%, 0% 80%, 0 10%);   
      &_btn {
        width: 272px;
        height: 78px;
        padding: 19px, 50px, 19px, 50px;
        gap: 10px;
        font-size: 24px;
        font-weight: 700;
        line-height: 40px;
        letter-spacing: 0em;
        text-align: center;
        color: #F8F200;
        background-color: #000000;
        font-family: Roboto;
      }
    }
  }
}
@media (min-width: 1920px)  {
  .container-header {
    width: 1280px;
  }
}
@media (min-width: 1024px) and (max-width: 1920px) {
    .layout {
      background-image: url("../assets/background_1024.jpg");
      animation: changebackground1024 20s infinite;
      &_container {
        padding: 0px 36px; 
        &_header {
          width: 952px;
        }  
      } 
    } 
}
@media (min-width: 320px) and (max-width: 1024px) {
    .layout {
      background-size: cover;
      background-repeat: no-repeat;
      height: 763px;
      width: 320px;
      &_container {
        align-items: center;
        box-sizing: border-box;
        padding: 0px 12px;  
        .container-header {
          width: 296px;
          flex-wrap: wrap;
          justify-content: center;
          &_сyberpunk-logo {
            width: 200px;
            height: 50px;
          }
          &_logo img { 
            width: 25px;
            height: 25px;
          } 
        }
        .container-banner {
          width: 320px;
          height: 207px;
          padding: 30px 38px;
          transform: translate(0px, 50px);
          clip-path: polygon(20% 0, 100% 0, 100% 20%, 100% 80%, 85% 100%, 0 100%, 0% 80%, 0 25%);
          &_btn {
            width: 244px;
            height: 60px;
            font-size: 20px;
            font-weight: 700;
            line-height: 40px;
            }
        }
      }
    }
}
</style>