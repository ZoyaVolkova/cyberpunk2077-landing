<template>
    <div class="layout1">
      <div class="layout1_container">
        <span class="header-font layout1_container_header">Найт-Сити изменит тебя навсегда!</span>
        <span class="layout1_container_game-description game-description color-gray">
          <span class="game-description_title">Cyberpunk 2077</span>
          — приключенческая ролевая игра, действие которой происходит в мегаполисе Найт-Сити, где власть, роскошь и модификации тела ценятся выше всего. 
          Ты играешь за V, наёмника в поисках устройства, позволяющего обрести бессмертие. 
          Ты сможешь менять киберимпланты, навыки и стиль игры своего персонажа, исследуя открытый мир, где твои поступки влияют на ход сюжета и всё, что тебя окружает.
        </span>
        <div class="layout1_container_images container-images">
          <img class="container-images_image1" src="../assets/city_1.png">
          <img class="container-images_image2" src="../assets/city_2.png">
          <img class="container-images_image3" src="../assets/city_3.png">
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Layout1Component',
}
</script>

<style scoped lang="scss">
.layout1 {
  width: 100%;
  padding: 70px 320px;
  box-sizing: border-box;
    &_container {
      display: flex;
      flex-direction: column;
      flex-wrap: wrap;
      &_header {
        margin-bottom: 25px;
      }     
      &_images {
        display: grid;
        justify-content: start;
        margin-top: 70px;
        img {
          clip-path: polygon(10% 0, 100% 0, 100% 20%, 100% 90%, 90% 100%, 0 100%, 0% 80%, 0 10%);
        }
      } 
    }
}
@media (min-width: 1920px)  {
  .container-images {
    grid-template-areas: "a c" "b c ";
    gap: 35px;
    margin-top: 55px;
    &_image1, &_image2 {
      width: 460px;
      height: 196px;
    }
    &_image1 {
      grid-area: a;
    }
    &_image2 {
      grid-area: b;
    }
    &_image3 {
      width: 788px;
      height: 424px;
      grid-area: c;
    }
  } 
}
@media (min-width: 1024px) and (max-width: 1920px) {
  .layout1 {
    padding: 70px 36px;
    .container-images {
      grid-template-areas: "a b" "c c ";
      gap: 32px;
      &_image1, &_image2 {
        width: 460px;
        height: 196px;
      }
      &_image1 {
        grid-area: a;
      }
      &_image2 {
        grid-area: b;
      }
      &_image3 {
        width: 952px;
        height: 424px;
        grid-area: c;
      }
    }
  } 
}
@media (min-width: 320px) and (max-width: 1024px) {
    .layout1 {
    padding: 70px 0px;
    padding-top: 120px;
    &_container {
      align-content: center;
      &_header {
        padding: 0px 12px;
      }
      .container-images {
        grid-template-areas: "a" "b" "c";
        gap: 32px;
        &_image1, &_image2 {
          width: 320px;
          height: 196px;
        }
        &_image1 {
          grid-area: a;
        }
        &_image2 {
          grid-area: b;
        }
        &_image3 {
          width: 320px;
          height: 424px;
          grid-area: c;
        }
      } 
    }
  }  
}
</style>