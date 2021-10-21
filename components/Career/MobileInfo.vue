<template>
  <section id="info">
    <div class="info__cv container">
      <h2 class="info__cv-steps-title">Как стать частью MOJAM</h2>
      <p class="info__cv-steps-subtitle">Четыре простых шага отделяют вас от работы над <br> игровыми сервисами, которые
        любят миллионы <br> геймеров по всему миру</p>
      <div class="info__cv-list flexColumn">
        <div class="info__cv-list-item">
          <h3 class="info__cv-list-item-step">Шаг 1</h3>
          <h3 class="info__cv-list-item-title">Отправить CV</h3>
          <div class="info__cv-list-item-subtitle flex">
            <img src="/career/info/time.svg" alt="time">
            <p>Среднее время ответа 2
              рабочих дня</p>
          </div>
        </div>
        <div class="info__cv-steps-load">
          <p>Загрузите свое CV на странице понравившейся вакансии</p>
        </div>
        <div class="info__cv-list-item">
          <h3 class="info__cv-list-item-step">Шаг 2</h3>
          <h3 class="info__cv-list-item-title">Прескрининг</h3>
          <div class="info__cv-list-item-subtitle flex">
            <img src="/career/info/time.svg" alt="time">
            <p>Фидбек в течение 2-х рабочих дней</p>
          </div>
        </div>
        <div class="info__cv-list-item">
          <h3 class="info__cv-list-item-step">Шаг 3</h3>
          <h3 class="info__cv-list-item-title">Техническое
            собеседование</h3>
          <div class="info__cv-list-item-subtitle flex">
            <img src="/career/info/time.svg" alt="time">
            <p>Фидбек в течение 3-х рабочих дней</p>
          </div>
        </div>
        <div class="info__cv-list-item">
          <h3 class="info__cv-list-item-step">Шаг 4</h3>
          <h3 class="info__cv-list-item-title">Получение оффера</h3>
          <div class="info__cv-list-item-subtitle flex">
            <img src="/career/info/time.svg" alt="time">
            <p>В течение 3-х рабочих дней</p>
          </div>
        </div>
      </div>

      <div class="info__cv-steps">
        <div class="info__cv-steps-items flexBetween">
          <div class="info__cv-steps-item flexColumn">
            <h3 class="info__cv-steps-item-title">Шаг 2.1</h3>
            <p class="info__cv-steps-item-subtitle">В редких случаях мы предлагаем выполнить <span>оплачиваемое тестовое
                    задание</span>, чтобы убедиться в профессионализме кандидата</p>
            <div class="info__cv-steps-item-times flex">
              <img src="/career/info/time.svg" alt="time">
              <p>от 7 до 14 дней</p>
            </div>
          </div>
          <div class="info__cv-steps-item flexColumn">
            <h3 class="info__cv-steps-item-title">Шаг 3.1</h3>
            <p class="info__cv-steps-item-subtitle">Часто, но не всегда, кандидаты проходят <span>финальное собеседование</span>
              с CEO или CTO.</p>
            <div class="info__cv-steps-item-times flex">
              <img src="/career/info/time.svg" alt="time">
              <p>Фидбэк в течение 3-х  <br>рабочих дней</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
name: "MobileInfo"
}
</script>

<style lang="scss" scoped>
@media screen and (max-width: 460px) {
  #info {
    height: 776rem;
  }
  .info {
    &__images {
      display: none;
    }

    &__cv {
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      &-list {
        align-items: initial;
        height: 100%;
        width: 100%;
        box-sizing: border-box;
        padding-left: 28rem;
        &:after {
          height: 332.8rem;
          left: 9.6rem;
          top: 23.5rem;
        }

        &-item {
          width: 71.2rem;
          padding-bottom: 65.2rem;
          padding-right: 20.8rem;
          &:last-child{
            padding-bottom: 55rem;
          }
          &:after {
            content: '';
            width: 4.8rem;
            border-radius: 50%;
            background-color: #F3BD4D;
            line-height: 1;
            top: 0;
            height: 4.8rem;
            font-size: 4.8rem;
          }

          &:nth-child(1) {
            &:after {
              left: -20.6rem;
              background-color: #41B7A8;
              top: 22rem;
            }
          }

          &:nth-child(3) {
            &:after {
              left: -20.6rem;
              top: 20rem;
            }
          }

          &:nth-child(4) {
            &:after {
              left: -20.6rem;
              top: 30rem;
            }
          }

          &:nth-child(5) {
            &:after {
              left: -20.6rem;
              top: 20rem;
            }
          }

          &-step {
            font-size: 5.4rem;
            line-height: 6.4rem;
            padding-bottom: 3.2rem;
          }

          &-title {
            font-size: 8rem;
            line-height: 9.2rem;
            padding-bottom: 6.8rem;
          }

          &-subtitle {
            p {
              width: 59.2rem;
              font-size: 4.8rem;
              line-height: 5.6rem;
            }

            img {
              width: 8rem;
              padding-right: 3.6rem;
            }
          }

          &:nth-child(2) {
            align-self: initial;
          }

          &:nth-child(4) {
            align-self: initial;
          }
        }

      }

      &-steps {
        grid-area: steps;

        &-load {
          width: 96rem;
          height: 27.6rem;
          top: 52.5rem;
          right: 3.5rem;
          padding: 0;
          p {
            width: 72rem;
            display: block;
            margin: auto;
            padding: 3rem 0;
            font-size: 6.4rem;
            line-height: 7.2rem;
          }
        }

        &-title {
          font-size: 9.6rem;
          line-height: 11.2rem;
          width: 100%;
          padding-top: 23.2rem;
          &:after{
            width: 40rem;
            height: 0.8rem;
            top: 35.6rem;
          }
        }

        &-subtitle {
          font-size: 4.8rem;
          line-height: 5.6rem;
          width: 100%;
          padding-left: 0;
          padding-bottom: 14.8rem;
        }

        &-items {
          flex-direction: column;
        }
        &-item{
          width: 112rem;
          height: 112rem;
          padding: 12rem;
          box-sizing: border-box;
          &-title{
            font-size: 6.4rem;
            line-height: 7.2rem;
          }
          &-subtitle{
            font-size: 6.4rem;
            line-height: 7.2rem;
          }
          &-times{
            p{
              font-size: 4.8rem;
              line-height: 5.6rem;
            }
            img{
              width: 8rem;
              padding-right: 3.6rem;
            }
          }
          &:first-child{
            margin-bottom: 12rem;
          }

        }


      }
    }

  }
}
</style>
