<template>
  <div class="layout4">
    <div class="layout4_container">
      <img class="layout4_container_image-covers" src="../assets/covers.jpg">
      <div class="layout4_container_box container-box">
        <span class="container-box_header">Купить игру Cyberpunk 2077</span>
        <div class="container-box_list1-container">
          <span class="container-box_list1-container_title">В комплект входит:</span>
          <ul class="container-box_list1-container_list container-list">
            <li><img src="../assets/logo/disk_logo.png">Футляр с игровыми дисками</li>
            <li><img src="../assets/logo/wysiwyg_logo.png">Футляр с кодом для загрузки игры и дисками (pc)</li>
            <li><img src="../assets/logo/collections_logo.png">Справочник с информацией об игровом мире</li>
          </ul>
        </div>
        <div class="container-box_list2-container">
          <span class="container-box_list2-container_title">Выберите платформу:</span>
          <ul class="container-box_list2-container_list container-list">
            <li><img class="container-list_logo-pc" src="../assets/logo/pc_logo.png"></li>
            <li><img class="container-list_logo-xbox" src="../assets/logo/xbox_logo.png"></li>
            <li><img class="container-list_logo-stadia" src="../assets/logo/stadia_logo.png"></li>
            <li><img class="container-list_logo-ps4" src="../assets/logo/ps4_logo.png"></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Layout4Component',
}
</script>

<style lang="scss">
.layout4 {
  width: 100%;
  background-color:  #000000;
  &_container {
    display: flex;
      .container-box {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        &_header {
          font-family: Archangelsk;
          letter-spacing: 0em;
          text-align: left;
          color: #FFFFFF;
        }
        &_list1-container_title, &_list2-container_title {
          font-family: Roboto;
          letter-spacing: 0em;
          text-align: left;
          color: #52BEDC;
        }
        .container-list {
          font-family: Roboto;
          letter-spacing: 0em;
          color: #FFFFFF;
          list-style: none;
          padding: 0;
          display: flex;
          flex-direction: column;
        }
        &_list1-container {
          &_list {
            li {
              display: flex;
              align-items: center;
              margin-bottom: 15px;
            }
            li:last-child {
              margin-bottom: 0px;
            }
          }
        }
        &_list2-container {
          .container-list {
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            justify-content: space-between;
            align-content: space-between;
            align-items: center;
            margin-top: 25px;
          }
        }
      }
  }
}
@media (min-width: 1024px) {
  .layout4 {
    width: 100%;
    height: 717px;
    &_container {
      &_image-covers {
        width: 944px;
        height: 717px; 
      }
      .container-box {
        padding: 70px 32px;
        &_header {
          font-size: 62px;
          font-weight: 400;
          line-height: 63px;
          width: 624px;
        }
        &_list1-container_title, &_list2-container_title {
          font-size: 24px;
          font-weight: 700;
          line-height: 28px;  
        }
        .container-list {
          font-size: 18px;
          font-weight: 400;
          line-height: 21px;
        }
        &_list1-container {
          margin-top: 15px;
          &_list {
            img {
              margin-right: 10px;
            }
          }
        }
        &_list2-container {
          width: 320px;
          height: 133px;
          li:nth-child(odd) {
            margin-right: 80px;
          }
        }
      }
    }
  }
}
@media (min-width: 1024px) and (max-width: 1920px) {
  .layout4 {
    width: 1024px;
    margin:0px;
    padding: 0px;
    &_container {
      width: 1024px;
      &_image-covers {
        width: 332px;
        height: 717px;
        content:url("../assets/covers_1024.png");
      }
    }
  }
}
@media (min-width: 320px) and (max-width: 1024px) {
  .layout4 {
    width: 320px;
    margin:0px;
    padding: 0px;
    &_container {
      width: 320px;
      flex-direction: column;
      &_image-covers {
        width: 320px;
        height: 198px;
        box-sizing: border-box;
      }
      .container-box {
        height: 587px;
        padding: 40px 12px 70px 12px;
        box-sizing: border-box;
        &_header {
          font-size: 30px;
          font-weight: 400;
          line-height: 31px;
        }
        &_list1-container_title, &_list2-container_title  {
          font-size: 20px;
          font-weight: 700;
          line-height: 23px;
        }    
        &_list1-container {
          font-size: 16px;
          font-weight: 400;
          line-height: 19px;
          img {
            margin-right: 18px;
          }
        }
        &_list2-container {
          .container-list {
            li {
              margin: 0px;
              display: flex;
              align-self: flex-start;
            }
            &_logo-pc {
              width: 62px;
              height: 35px;
              margin-bottom: 40px;
            }
            &_logo-xbox {
              width: 178px;
              height: 35px;
            }
            &_logo-stadia {
              width: 58px;
              height: 50px;
            }
            &_logo-ps4 {
              width: 169px;
              height: 35px;
            }
          }
        }
      }
    }
  }
}
</style>