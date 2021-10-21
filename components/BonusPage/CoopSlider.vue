<template>
  <section id="coop-slider">
    <div class="container coop-slider">
      <div class="coop-slider__block">
        <div class="coop-slider__items">
          <div class="coop-slider__row hide-mobile">
            <div class="coop-slider__item coop-slider__item-top1">
              <div class="coop-slider__info">
                <h3 class="coop-slider__item-title">Пейнтбол</h3>
                <p class="coop-slider__item-subtitle">май 2021</p>
              </div>
              <img src="/bonus/paintbool.png" alt="paintbool" />
            </div>
            <div
              class="coop-slider__item coop-slider__item-row coop-slider__item-top2"
            >
              <div class="coop-slider__info">
                <h3 class="coop-slider__item-title">Печенеги</h3>
                <p class="coop-slider__item-subtitle">март 2021</p>
              </div>
              <img src="/bonus/photo.png" alt="photo" />
            </div>
            <div
              class="coop-slider__item coop-slider__item-cr coop-slider__item-top3"
            >
              <div class="coop-slider__info">
                <h3 class="coop-slider__item-title">Карпаты</h3>
                <p class="coop-slider__item-subtitle">ноябрь 2020</p>
              </div>
              <img src="/bonus/forest.png" alt="forest" />
            </div>
          </div>
          <div class="coop-slider__item-middle flexColumn">
            <h2 class="coop-slider__title">
              Корпоративный отдых
            </h2>
            <p class="coop-slider__text">
              Мы уделяем большое внимание созданию комфортных условий для наших
              сотрудников. Наша команда - вторая семья, с которой мы не только
              продуктивно работаем, но и регулярно проводим время в неформальной
              обстановке. Это помогает не только интересно провести время, но и
              улучшить взаимопонимание и сплаченность коллектива
            </p>
          </div>
          <div class="coop-slider__row flexAround hide-mobile">
            <div
              class="coop-slider__item coop-slider__item-row coop-slider__item-bot1"
            >
              <div class="coop-slider__info">
                <h3 class="coop-slider__item-title">Пикник</h3>
                <p class="coop-slider__item-subtitle">апрель 2021</p>
              </div>
              <img src="/bonus/piknik.png" alt="Пикник" />
            </div>
            <div
              class="coop-slider__item coop-slider__item-row coop-slider__item-bot2"
            >
              <div class="coop-slider__info">
                <h3 class="coop-slider__item-title">Картинг</h3>
                <p class="coop-slider__item-subtitle">ноябрь 2020</p>
              </div>
              <img src="/bonus/karting.png" alt="photo" />
            </div>
          </div>
          <div class="coop-slider__mobile">
            <div class="coop-slider__mobile-item">
              <div class="coop-slider__mobile-info">
                <h3 class="coop-slider__mobile-title">Пикник</h3>
                <p class="coop-slider__mobile-subtitle">апрель 2021</p>
              </div>
              <img src="/bonus/piknik.png" alt="Пикник" />
            </div>
            <div class="coop-slider__mobile-pagination pagination">
              <span class="pagination__item"></span
              ><span class="pagination__item pagination__item-active"></span
              ><span class="pagination__item"></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
#coop-slider {
  width: 100%;
  height: 85rem;
  .flexAround {
    display: flex;
    justify-content: space-around;
    align-items: flex-end;
  }
}
.coop-slider {
  padding-top: 6rem;
  &__title {
    font-size: 3rem;
    line-height: 3.4rem;
    position: relative;
    margin-bottom: 3.3rem;

    &::after {
      content: "";
      position: absolute;
      top: 3.8rem;
      right: 0;
      left: 0;
      bottom: 0;
      width: 10rem;
      height: 0.2rem;
      background: $green;
    }
  }
  &__text {
    font-size: 1.6rem;
    line-height: 1.8rem;
    font-weight: 300;
    color: $black;
    width: 57rem;
    margin-left: auto;
    letter-spacing: 0;
  }
  &__items {
    display: flex;
    flex-direction: column;
  }
  &__row {
    padding-top: 1px;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  &__item {
    display: flex;
    flex-direction: column;
    &-top1 {
      position: relative;
      top: -1.3rem;
      .coop-slider__info {
        margin-bottom: 2.6rem;
      }
    }
    &-top2 {
      margin-top: -10.5rem;
      margin-left: 1.1rem;
      .coop-slider__info {
        margin-left: 2.9rem;
      }
    }
    &-top3 {
      margin-top: 8.5rem;
      .coop-slider__info {
        margin-top: 2.5rem;
      }
    }
    &-bot1 {
      margin-left: 12rem;
      .coop-slider__info {
        margin-left: 3rem;
        margin-top: -0.5rem;
      }
    }
    &-bot2 {
      margin-left: 4rem;
      .coop-slider__info {
        margin-left: 3rem;
        margin-top: -0.5rem;
      }
    }
    &-row {
      display: flex;
      flex-direction: row-reverse;
    }
    &-cr {
      flex-direction: column-reverse;
    }
    &-middle {
      width: 67.2rem;
      display: flex;
      flex-direction: column;
      margin-top: 1rem;
      margin-bottom: 5.4rem;
      margin-left: auto;
      margin-right: 21rem;
    }

    &-title {
      font-size: 2rem;
    }
    &-subtitle {
      font-size: 1.6rem;
      padding-top: 0.4rem;
    }
  }
}
@media screen and (max-width: 460px) {
  #coop-slider {
    width: 100%;
    height: auto;
  }
  .coop-slider {
    padding: 21rem 0;
    &__mobile {
      display: none;
    }
    &__title {
      font-size: 9.6rem;
      line-height: 11.2rem;
      position: relative;
      margin-bottom: 21rem;
      margin-left: 0;
      &:after {
        content: "";
        position: absolute;
        top: 12rem;
        right: 0;
        left: 0;
        bottom: 0;
        width: 40rem;
        height: 1rem;
        background: #41b7a8;
      }
    }
    &__text {
      font-size: 5.6rem;
      line-height: 6.4rem;
      width: 100%;
      margin: 0;
      margin-bottom: 23rem;
    }
    &__row {
      order: 2;
    }
    &__item {
      &-row {
        order: 2;
      }
      &-middle {
        width: 100%;
        margin: 0;
        order: 0;
      }
    }
    &__mobile {
      display: block;
      position: relative;
      left: -8rem;
      width: 144rem;
      height: 120rem;
      &-item {
        width: 100%;
        height: 100%;
      }
      &-info {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        box-sizing: border-box;
        padding: 2.4rem 6rem;
        background: rgba(14, 14, 14, 0.5);
      }
      &-title {
        color: $white;
        font-size: 8rem;
        line-height: 9rem;
        font-weight: 400;
        letter-spacing: 0;
      }
      &-subtitle {
        color: $white;
        font-size: 6.4rem;
        line-height: 7.2rem;
        font-weight: 300;
        letter-spacing: 0;
      }
      &-pagination {
        position: absolute;
        bottom: 6.8rem;
        left: 0;
        right: 0;
      }
    }
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }

  .hide-mobile {
    display: none !important;
  }
  .pagination {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: center;
    &__item {
      margin: 0 4rem;
      width: 3.2rem;
      height: 3.2rem;
      background: rgba(255, 254, 254, 0.5);
      border-radius: 50%;
      &-active {
        background: $white;
        scale: 1.5;
      }
    }
  }
}
</style>
