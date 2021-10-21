<template>
  <section id="technologies">
    <div class="technologies">
      <div class="technologies__lang">
        <div class="flexBetween">
          <img src="/vacancy/laravel.svg" alt="laravel" style="width: 10.4rem;">
          <img src="/vacancy/symfony.svg" alt="symfony" style="width: 5.1rem;">
          <img src="/vacancy/vue.svg" alt="vue" style="width: 8.6rem;">
          <img src="/vacancy/node.svg" alt="node" style="width: 8rem;">
        </div>
        <div class="technologies__images flexBetween">
          <img src="/vacancy/php-black.svg" alt="php" style="width: 7.7rem;">
          <img src="/vacancy/js.svg" alt="js" style="width: 4.1rem;">
          <img src="/vacancy/html-css.svg" alt="html" style="width: 6.6rem;">
        </div>
        <div class="technologies__images">
          <img src="/vacancy/yii.svg" alt="yii" style="width: 16.5rem;">
        </div>
      </div>
      <div class="technologies__info">
        <img src="/home/technologies/points.svg" alt="points" class="technologies__info-img">
        <h3 class="technologies__info-title">Технологии</h3>
        <p class="technologies__info-subtitle">Мы используем самые современные решения и постоянно осваиваем новые
          технологии, чтобы подарить лучший пользовательский опыт нашему комьюнити </p>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
#technologies {
  width: 100%;
  height: 44.2rem;
  background: #1D1D1D;
}

.technologies {
  display: grid;
  grid-template-columns: 61rem 81rem;
  width: 100%;
  height: 100%;

  &__lang {
    background: linear-gradient(93.58deg, #FF9F42 6.21%, #EFC751 97.05%);
    padding-top: 12rem;
    padding-left: 13rem;
    padding-right: 4rem;
  }

  &__images {
    padding-top: 3.6rem;
    padding-right: 18rem;
    padding-bottom: .5rem;
  }

  &__info {
    padding-top: 3.5rem;
    padding-left: 12rem;
    position: relative;

    &-img {
      position: absolute;
      width: 20.2rem;
      right: 1.3rem;
    }
    &-title {
      font-size: 3rem;
      padding-top: 8rem;
      line-height: 3.4rem;
      color: $white;
      position: relative;
      &::after {
        content: '';
        position: absolute;
        top: 11.5rem;
        bottom: 0;
        left: 0;
        right: 0;
        width: 10rem;
        height: .2rem;
        background: $orange;
      }
    }
    &-subtitle {
      font-size: 1.6rem;
      font-weight: 300;
      line-height: 1.8rem;
      color: #F1F1F1;
      padding-top: 5rem;
      padding-left: 10rem;
      letter-spacing: 0;
      width: 48rem;
    }
  }
}
</style>
