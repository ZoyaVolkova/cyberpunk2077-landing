<template>
    <div class="layout3">
      <img class="layout3_grain" src="../assets/grain_black-yellow.jpg">
      <div class="layout3_container">
        <div class="layout3_container_box1 container-box1">
          <img class="container-box1_image-tv" src="../assets/tv.png">
          <div class="container-box1_logo-container">
            <img class="container-box1_logo-container_image-hp" src="../assets/logo/hp_logo.png">
            <svg width="92" height="21" viewBox="0 0 92 21" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path d="M91 1.28149L1 19.9012" stroke="black"/>
              <path d="M90.8938 20.1829L1.1065 0.999834" stroke="black"/>
            </svg>
            <img class="container-box1_logo-container_logo-cyberpunk" src="../assets/logo/Cyberpunk_2077_logo.png">
          </div>
        </div>
        <div class="layout3_container_box2 container-box2 ">
          <span class="container-box2_header">Полное погружение вместе с HP</span>
          <span class="container-box2_text">Погрузись в современные экшен-игры с реалистичным изображением с помощью монитора с диагональю 23,8 дюйма, 
            созданном для отображения максимально насыщенных цветов.Успевай реагировать на любые события с временем отклика 1 мс и частотой в 144 Гц!
          </span>
          <ul class="container-box2_list">
            <li><img class="container-box2_list_logo-colors" src="../assets/logo/colors_logo.png">Яркие насыщенные цвета</li>
            <li><img class="container-box2_list_logo-stars" src="../assets/logo/stars_logo.png">Кристальная четкость изображения</li>
            <li><img class="container-box2_list_logo-squares" src="../assets/logo/squares_logo.png">Быстрые движения и плавный геймплей</li>
          </ul>
          <button class="container-box2_list_btn">Подробнее</button>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Layout3Component',
}
</script>

<style lang="scss">
.layout3 {
  width: 100%;
  background-color: #F8F200;
  &_grain {
    width: 100%;
    height: 70px;
    object-fit: cover;
  }
  &_container {
    display: flex;
    justify-content: space-between;
    box-sizing: border-box;
    .container-box1 {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      margin-right: 32px;
      &_logo-container {
        width: 540px;
        height: 80px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        &_image-hp {
          width: 80px;
          height: 80px;
        }
        &_logo-cyberpunk {
          width: 320px;
          height: 80px;
        }
      }

    }
    .container-box2 {
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      &_header {
        font-family: Archangelsk;
        font-size: 62px;
        font-weight: 400;
        line-height: 63px;
        letter-spacing: 0em;
        text-align: left;
        width: 560px;
      }
      &_text {
        font-family: Roboto;
        font-size: 18px;
        font-weight: 400;
        line-height: 34px;
        letter-spacing: 0em;
        text-align: left;
        width: 624px;
      }
      &_list {
        padding: 0;
        list-style: none;
        font-family: Roboto;
        font-size: 18px;
        font-weight: 400;
        line-height: 21px;
        letter-spacing: 0em;
        text-align: left;
        li {
          display: flex;
          align-items: center;
          margin-bottom: 15px;
        }
        li:last-child {
          margin-bottom: 0px;
        }
        img {
          margin-right: 10px;
        }
        &_btn {
          width: 194px;
          height: 59px;
          padding: 15px, 50px, 15px, 50px;
          background: #000000;
          font-family: Roboto;
          font-size: 18px;
          font-weight: 700;
          line-height: 21px;
          letter-spacing: 0em;
          text-align: center;
          color: #F8F200;
        }
      }
      
    }
  }
}
@media (min-width: 1920px)  {
  .layout3 {
    height: 746px;
    &_container {
      padding: 70px 320px;
      height: 676px;
      .container-box1 {
        &_image-tv {
          width: 624px;
          height: 430px;
        }
      }
    }
  }
}
@media (min-width: 1024px) and (max-width: 1920px) {
  .layout3 {
    width: 1024px;
    height: 866px;
    &_container {
      width: 1024px;
      height: 796px;
      padding: 0px 36px;
      justify-content: space-between;
      align-items: center;
      .container-box1 {
        margin: 0px;
        height: 571px;
        &_image-tv {
          width: 460px;
          height: 317px;
        }
        &_logo-container {
          width: 320px;
          height: 230px;
          box-sizing: border-box;
          flex-direction: column;
          svg {
            margin-top: 25px;
            margin-bottom: 25px;
          }
        }
      }
      .container-box2 {
        width: 460px;
        height: 656px;
        &_header {
          width: 460px;
        }
        &_text {
          margin-top: 25px;
          margin-bottom: 25px;
          width: 460px;
        }
      }
    }
  }
}

@media (min-width: 320px) and (max-width: 1024px) {
  .layout3 {
    width: 320px;
    &_container {
      width: 320px;
      padding: 70px 12px;
      justify-content: space-between;
      align-items: center;
      flex-direction: column;
      .container-box1 {
        margin: 0px;
        &_image-tv {
          width: 296px;
          height: 273px;
        }
        &_logo-container {
          width: 296px;
          box-sizing: border-box;
          &_image-hp {
            width: 43.85px;
            height: 44px;
          }
          svg {
            width: 45px;
            height: 11px;
          }
          &_logo-cyberpunk {
            width: 175.41px;
            height: 44px;
          }
        }
      }
      .container-box2 {
        width: 296px;
        &_header {
          width: 296px;
          font-size: 30px;
          font-weight: 400;
          line-height: 31px;
        }
        &_text {
          margin-top: 25px;
          margin-bottom: 25px;
          width: 296px;
          font-size: 16px;
          font-weight: 400;
          line-height: 32px;
        }
        &_list {
          &_btn {
            margin-top: 40px;
            font-size: 16px;
            font-weight: 700;
            line-height: 19px;
            width: 184px;
          }
        }
      }
    }
  }
}
</style>