<template>
  <div class="kit-wrap">
    <div class="kit_vito">
      <img class="kit_vito-img" src="src/assets/img/vito.png">
    </div>
    <div class="kit_info">
      <h2 class="kit_info-title">НАБОР «ПОСЫЛКА С КОНТРАБАНДОЙ»</h2>
      <div class="kit_info-btn">
        <button>Бесплатные сервера</button>
        <button>Подписочный сервер</button>
      </div>
      <div class="kit_info-items">
        <div class="kit_info_item" v-for="item in list">
          <div class="kit_info_item-name">
            <img class="kit_info_item-name-img" :src="item.icon">
            <h3 class="kit_info_item-name-title">{{ item.name }}</h3>
          </div>
          <div class="kit_info_item-meaning">
            <p class="kit_info_item-meaningOne">{{ item.meaningOne }}</p>
            <p class="kit_info_item-meaningTwo">{{ item.meaningTwo }}</p>
          </div>
        </div>
      </div>
      <div class="kit_info-box">
        <img src="src/assets/img/box.png">
        <div class="kit_info-box-pay">
          <span>399 ₽</span>
          <button>ПРИОБРЕСТИ</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "kit",
  data: () => ({
    list: [
      {
        name: 'Игровое время',
        icon: 'src/assets/img/icon/time.png',
        meaningOne: '-',
        meaningTwo: '30 дней'
      },
      {
        name: 'Запечатанный набор инструментов',
        icon: 'src/assets/img/icon/tulbox.png',
        meaningOne: '1',
        meaningTwo: '1'
      },
      {
        name: 'Хрупкая чистая руна 10-й ступени',
        icon: 'src/assets/img/icon/fragile.png',
        meaningOne: '1',
        meaningTwo: '-'
      },
      {
        name: 'Большой символ изобилия творца',
        icon: 'src/assets/img/icon/big-simvol.png',
        meaningOne: '10',
        meaningTwo: '-'
      },
      {
        name: 'Мана-батарея',
        icon: 'src/assets/img/icon/mana.png',
        meaningOne: '-',
        meaningTwo: '20'
      },
      {
        name: 'Модуль памяти',
        icon: 'src/assets/img/icon/modul.png',
        meaningOne: '-',
        meaningTwo: '10'
      },
      {
        name: 'Помощник Вито',
        icon: 'src/assets/img/icon/vito.png',
        meaningOne: '1',
        meaningTwo: '1'
      },
    ]
  })
}
</script>

<style lang="scss">
.kit {
  &-wrap {
    display: flex;
    z-index: 1;
  }
  &_vito, &_info {
    width: 50%;
  }
  &_vito {
    display: flex;
    justify-content: center;
    align-items: center;
    position: relative;
    &-img {
      position: relative;
      z-index: 2;
    }
  }
  &_vito:before {
    content: '';
    position: absolute;
    top: 50%; left: 50%;
    transform: translate3d(-50%, -50%, 0);
    width: 680px;
    height: 680px;
    border-radius: 686px;
    border: 1px solid #000;
    opacity: 0.2;
    background: #416DF4;
    mix-blend-mode: lighten;
    filter: blur(100px);
    z-index: 1;
  }
  &_info {
    &-title {
      color: #416DF4;
      font-size: 30px;
      font-weight: 700;
      line-height: normal;
      margin-bottom: 40px;
    }
    &-btn {
      display: flex;
      justify-content: flex-end;
      gap: 11px;
      margin-bottom: 9px;
      button {
        border: 1px solid rgba(103, 29, 0, 0.48);
        background: rgba(0, 0, 0, 0.55);
        color: #671D00;
        text-align: center;
        font-size: 12px;
        font-style: normal;
        font-weight: 400;
        line-height: normal;
      }
    }
    &-items {
      display: flex;
      flex-direction: column;
      gap: 1px;
    }
    &_item {
      display: flex;
      padding: 5px;
      border-radius: 1px;
      border: 1px solid rgba(103, 29, 0, 0.48);
      background: rgba(0, 0, 0, 0.55);
      &-name, &-meaning {
        display: flex;
        align-items: center;
      }
      &-name {
        width: 60%;
        &-img {
          width: 64px;
          height: 64px;
          margin-right: 20px;
        }
        &-title {
          color: #FFF;
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: normal;
        }
      }
      &-meaning {
        width: 40%;
        justify-content: space-around;
        p {
          width: 60px;
          text-align: center;
        }
      }
    }
    &-box {
      display: flex;
      align-items: flex-end;
      &-pay {
        display: flex;
        flex-direction: column;
        padding-bottom: 45px;
        span {
          color: #FFF;
          font-size: 50px;
          font-style: normal;
          font-weight: 400;
          line-height: normal;
        }
        button {
          border-radius: 7px;
          border: 0;
          padding: 12px 15px;
          background: #FCFF00;
          color: #000;
          text-align: center;
          font-size: 16px;
          font-weight: 400;
          line-height: normal;
        }
      }
    }
  }
}
</style>