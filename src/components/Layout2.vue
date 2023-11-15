<template>
  <div class="layout2">
    <img class="layout2_grain" src="../assets/grain_white-black.jpg">
    <div class="layout2_container">
      <div class="layout2_container_box1 container-box1">
        <img class="container-box1_image-action" src="../assets/action.png">
        <span class="container-box1_header header-font color-white">Играй и выигрывай!</span>
      </div>
      <span class="layout2_container_game-description game-description color-white">Играй в <span class="game-description_title">Cyberpunk 2077</span>
      и получи возможность выиграть консоль <span class="game-description_title">Xbox Series X</span> или <span class="game-description_title">Sony PlayStation 5!</span> 
      Заполни форму ниже и приложи скриншот о покупке игры. Итоги розыгрыша будут подведены 1 февраля. Удачи! ;)
      </span>
      <div class="layout2_container_box2 container-box2">
        <form class="container-box2_form" @submit.prevent="sendForm">
          <input class="container-box2_form_name" type="text" placeholder="Как тебя зовут?" v-model="form.name"/>
          <input class="container-box2_form_email" type="text" placeholder="Твой е-mail" v-model="form.email"/>
          <input-file v-model="form.file"></input-file>
          <button class="container-box2_form_send-btn">Отправить</button>
          <checkbox></checkbox>
        </form>
      </div>
      <img class="layout2_container_image-prize">
    </div>
  </div>
</template>

<script>
import InputFile from './InputFile.vue'
import Checkbox from './Checkbox.vue'
export default {
  name: 'Layout2Component',
  components: {
    InputFile, Checkbox
  },
  data() {
    return {
      form: {}
    }
  },
  methods: {
    sendForm() {
      console.log(this.form)
    }
  }

}
</script>

<style scoped lang="scss">
.layout2 {
  width: 100%;
  background-color:  #000000;
  &_grain {
    width: 100%;
    height: 70px;
    object-fit: cover;
  }
  &_container {
    display: grid;
    .container-box1 {
      display: flex; 
      grid-area: a;
      &_image-action {
      width: 132px;
      height: 132px;
      margin-right: 32px;
      }
    }
    &_game-description {
      grid-area: b;
    }
    .container-box2 {
      display: flex; 
      align-items: flex-end;
      grid-area: c;
      &_form {
        font-family: Roboto;
        font-size: 18px;
        font-weight: 300;
        color: #ffffff;
        line-height: 21px;
        letter-spacing: 0em;
        text-align: left;
        display: flex;
        flex-direction: column;
        width: 460px;
        height: 383px;
        justify-content: space-between;
        input[type=text], input[type=text]::placeholder {
          font-family: Roboto;
          font-size: 18px;
          font-weight: 300;
          color: #ffffff;
          line-height: 21px;
          letter-spacing: 0em;
          text-align: left;
        }
        input[type=text]:focus::placeholder {
          opacity: 0;
        }
        input[type=text]{
          background-color: transparent;
          padding-bottom: 13px;
          border: none;
          border-bottom: 1px solid #777777;
          outline: none;
        }
        &_send-btn {
          background-color: #F8F200;
          width: 192px;
          height: 59px;
          padding: 15px, 50px, 15px, 50px;
          font-family: Roboto;
          font-size: 18px;
          font-weight: 700;
          line-height: 21px;
          letter-spacing: 0em;
          text-align: center;
        }
      }
    }
    &_image-prize {
      width: 788px;
      height: 456px;
      grid-area: d;
    }
  }
}
@media (min-width: 1920px)  {
  .layout2 {
    &_container {
      padding: 15px 320px 70px 320px;
      grid-template-areas: "a a" "b b" "c d";
      gap: 25px;
      .container-box1 {
        align-items: center;
        &_header {
          align-self: flex-end;
        }
      }
      &_image-prize {
        content:url("../assets/prize.png");
        width: 788px;
        height: 456px;
      }
    }
  }
}
@media (min-width: 1024px) and (max-width: 1920px) { 
  .layout2 {
    &_container {
      height: 1023px;
      box-sizing: border-box;
      padding: 15px 36px 70px 36px;
      grid-template-areas: "a d" "b d" "c d";
      gap: 25px;
      .container-box1 {
        flex-direction: column;
        align-items: flex-start;
        &_image-action {
          margin-bottom: 15px;
        }
        &_header {
          align-self: flex-end;
        }
      }
      &_image-prize {
        content:url("../assets/prize_1024.png");
        width: 460px;
        height: 858px;
        align-self: flex-end;
      }
    }
  }
}
@media (min-width: 320px) and (max-width: 1024px) {
  .layout2 {
    width: 320px;
    box-sizing: border-box;
    &_container {
      width: 320px;
      grid-template-columns: 320px;
      box-sizing: border-box;
      padding: 6px 12px 70px 12px;
      grid-template-areas: "a" "d" "b" "c" ;
      gap: 25px;
      .container-box1 {
        flex-direction: column;
        &_image-action {
          width: 62px;
          height: 62px;
        }
        &_header {
          transform: translate(0px, 143px);
        }
      }
      &_game-description {
        width: 296px;
        padding: 0px;
        font-size: 16px;
        font-weight: 400;
        line-height: 32px;
        margin-bottom: 45px;
        &_title { 
          font-size: 16px;
          font-weight: 700;
          line-height: 32px;
        }
      }
      .container-box2 {
        &_form {
          input[type=text], input[type=text]::placeholder {
            width: 296px;  
            box-sizing: border-box;
            font-size: 12px;
            font-weight: 300;
            line-height: 14px;
          }
          &_send-btn {
            font-size: 16px;
            font-weight: 700;
            line-height: 19px;
          }
        }
      }
      &_image-prize {
        content:url("../assets/prize_320.png");
        width: 296px;
        height: 130.85px;
        transform: translate(0px, -70px);
      }
    }
  }
}
</style>
