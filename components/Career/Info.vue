<template>
  <section id="info" v-if="width >   400">
    <div class="info__images flexBetween">
      <img src="/career/info/points.svg" alt="points" class="info__images-left">
      <img src="/career/info/points2.svg" alt="points" class="info__images-right">
    </div>
    <div class="info__cv container">
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
        <div class="info__cv-steps-load">
          <p>Загрузите свое CV на странице понравившейся вакансии</p>
        </div>
        <h2 class="info__cv-steps-title">Как стать частью MOJAM</h2>
        <p class="info__cv-steps-subtitle">Четыре простых шага отделяют вас от работы над игровыми сервисами, которые
          любят миллионы геймеров по всему миру</p>
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
              <p>Фидбэк в течение 3-х рабочих дней</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <MobileInfo v-else/>
</template>
<script>
import MobileInfo from "@/components/Career/MobileInfo";

export default {
  components: {
    MobileInfo
  },
  data: () => ({
    width: 0,
  }),
  methods: {
    updateWidth() {
      console.log(this.width)
      this.width = document.documentElement.clientWidth;
    },
  },
  created() {
    window.addEventListener('resize', this.updateWidth);
  },
}
</script>
<style lang="scss">
#info {
  width: 100%;
  height: 75.6rem;
  background: $bgDark;
  padding-top: 2rem;
}

.info {
  &__images {
    &-left {
      width: 16.7rem;
    }

    &-right {
      position: relative;
      right: 21.8rem;
      top: 1rem;
      width: 9.2rem;
    }
  }

  &__cv {
    display: grid;
    grid-template-columns: 53rem 58rem;
    grid-gap: 7rem;

    &-list {
      padding-left: 4.6rem;
      padding-top: 5rem;
      height: 56rem;
      position: relative;

      &-item {
        width: 20rem;
        position: relative;

        &-step {
          color: $green;
          font-size: 1.6rem;
          line-height: 1.8rem;
        }

        &-title {
          color: $white;
          font-size: 2rem;
          line-height: 2.3rem;
          margin-top: .5rem;
        }

        &-subtitle {
          margin-top: 2rem;

          p {
            color: #87898E;
            font-size: 1.2rem;
            margin-left: 1rem;
          }

          img {
            width: 2rem;
          }
        }

        &:nth-child(2) {
          align-self: flex-end;
        }

        &:nth-child(2)::after {
          left: -4.15rem;
          color: $orange;
        }

        &:nth-child(4) {
          align-self: flex-end;
          position: relative;
          bottom: 3rem;
        }

        &:nth-child(4)::after {
          left: -4.15rem;
          color: $orange;
        }

        &:nth-child(3)::after {
          color: $orange;
          top: 6rem;
        }

        &::after {
          content: "•";
          position: absolute;
          top: 3.3rem;
          right: 0;
          left: 24.25rem;
          bottom: 0;
          font-size: 5rem;
          color: #41B7A8;
          z-index: 1;
        }
      }

      &::after {
        position: absolute;
        content: "";
        top: 9.5rem;
        left: 30rem;
        right: 0;
        bottom: 0;
        width: 0.2rem;
        background: #41B7A8;
        height: 48.4rem;
      }
    }

    &-steps {
      position: relative;

      &-title {
        font-size: 3rem;
        line-height: 3.4rem;
        color: $white;
        width: 34rem;
        position: relative;
        bottom: 1rem;

        &::after {
          content: '';
          position: absolute;
          top: 3.6rem;
          left: 0;
          right: 0;
          bottom: 0;
          width: 10rem;
          height: .2rem;
          background: $green;
        }
      }

      &-subtitle {
        width: 38.1rem;
        font-size: 1.6rem;
        line-height: 1.8rem;
        padding-top: 5.5rem;
        color: #F1F1F1;
        padding-left: 10rem;
        letter-spacing: 0;
      }

      &-load {
        width: 18rem;
        height: 6.9rem;
        border: .1rem solid $green;
        position: absolute;
        right: 60.5rem;
        top: 2.5rem;
        padding: 0 3rem;

        p {
          color: $white;
          font-size: 1.6rem;
          line-height: 1.8rem;
          font-weight: 300;
          padding-top: .6rem;
          letter-spacing: 0;
        }
      }

      &-items {
        padding-top: 10rem;
      }

      &-item {
        width: 22rem;
        height: 22rem;
        padding: 3rem;
        border: .1rem solid $green;

        &-title {
          color: $green;
          font-size: 1.6rem;
          line-height: 1.8rem;
        }

        &-subtitle {
          font-size: 1.6rem;
          line-height: 1.8rem;
          color: $white;
          font-weight: 300;
          letter-spacing: 0;
          padding-bottom: 7rem;

          span {
            color: $green;
          }
        }

        &-times {
          img {
            width: 2rem;
          }

          p {
            color: #87898E;
            font-size: 1.2rem;
            line-height: 1.4rem;
            margin-left: .9rem;
          }
        }
      }
    }
  }
}

</style>
