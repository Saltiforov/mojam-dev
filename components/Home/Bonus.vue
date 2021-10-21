<template>
  <section
    id="bonus"
    :style="
      homePage ? 'padding-top: 11rem;' : 'padding-top: 5rem; height: 59.5rem;'
    "
  >
    <div :class="homePage ? 'container' : 'container-s'">
      <h2 class="title afterText ">
        Бонусы сотрудникам
      </h2>
      <p class="subtitle bonus__subtitle">
        Кроме высокой зарплаты, наши сотрудники получают и другие приятные
        бонусы
      </p>
      <div class="bonus__items">
        <div class="bonus__item item">
          <img
            src="/home/bonus/bonus1.png"
            alt="bonus"
            class="bonus__item-image"
          />
          <h4 class="bonus__item-text">
            Юридическое и бухгалтерское обслуживание
          </h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus2.png" alt="bonus" />
          <h4 class="bonus__item-text">
            Работа <br />
            из дома
          </h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus3.png" alt="bonus" />
          <h4 class="bonus__item-text">
            Свободный график
          </h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus4.png" alt="bonus" />
          <h4 class="bonus__item-text">
            Курсы и повышение квалификации
          </h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus5.png" alt="bonus" />
          <h4 class="bonus__item-text">Минимум бюрократии</h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus6.png" alt="bonus" />
          <h4 class="bonus__item-text">
            Тренажерный зал и бассейн
          </h4>
        </div>
        <div class="bonus__item item">
          <img src="/home/bonus/bonus7.png" alt="bonus" />
          <h4 class="bonus__item-text">
            Оплачиваемый отдых
          </h4>
        </div>
      </div>
      <div class="bonus__buttons" v-if="homePage">
        <button class="button__orange">Бонусы сотрудникам</button>
        <button class="button__dark bonus__buttons-light">Наша Команда</button>
      </div>
    </div>
    <img src="/points.svg" alt="points" class="bonus__point" />
  </section>
</template>
<script>
export default {
  props: ["homePage"]
};
</script>
<style lang="scss">
#bonus {
  width: 100%;
  height: 69.5rem;
  padding-top: 11rem;
  position: relative;
}

.bonus {
  &__subtitle {
    padding-top: 3rem;
    width: 36rem;
    padding-left: 10rem;
  }

  &__items {
    display: grid;
    grid-template-columns: 18rem 18rem 18rem 18rem;
    grid-gap: 2rem;
    grid-template-rows: 18rem 18rem;
    justify-content: center;
    padding-top: 6rem;
  }

  &__item {
    background-color: #f5f8fc;
    padding: 1.6rem;
    width: 14.8rem;
    flex-direction: column;
    display: flex;
    height: 14.8rem;
    align-items: flex-start;
    justify-content: space-between;

    img {
      width: 3rem;
    }

    &-image {
      width: 3rem;
    }

    &-text {
      color: $black;
      font-size: 2rem;
      line-height: 2.3rem;
      font-weight: bold;
      width: 14rem;
    }
  }

  &__buttons {
    display: flex;
    align-items: center;
    padding-top: 6rem;
    width: 40rem;
    justify-content: space-between;
    margin: auto;

    &-light {
      color: $black;
    }
  }

  &__point {
    position: absolute;
    bottom: 13rem;
    right: 23rem;
    width: 18rem;
  }
}

@media screen and (max-width: 460px) {
  #bonus {
    height: 100% !important;
  }
  .container-s {
    width: 128rem;
  }
  .title {
    font-size: 9.6rem;
    line-height: 11.2rem;
    padding-bottom: 16rem;

    &:after {
      content: "";
      position: absolute;
      top: 12.8rem;
      width: 40rem;
      height: 0.8rem;
    }
  }
  .bonus {
    &__subtitle {
      font-size: 5.6rem;
      line-height: 6.4rem;
      width: 100%;
      padding-left: 0;
    }

    &__items {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      padding-bottom: 24rem;
    }

    &__item {
      box-sizing: border-box;
      width: 72rem;
      height: 72rem;
      padding: 6rem;
      margin-bottom: 10.4rem;

      &:nth-child(2) {
        position: relative;

        &:after,
        &:before {
          content: "";
          position: absolute;
          width: 6.8rem;
          height: 16rem;
          top: 29rem;
        }

        &:after {
          left: -23.6rem;
          background-repeat: no-repeat;
          background-image: url(static/slider-left.svg);
        }

        &:before {
          right: -23.6rem;
          background-repeat: no-repeat;
          background-image: url(static/slider-right.svg);
        }
      }

      img {
        width: 12rem;
      }

      &-text {
        font-size: 8rem;
        line-height: 9.2rem;
        width: 100%;
      }
    }
    &__buttons {
      display: none;
    }
  }
}
</style>
