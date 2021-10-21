<template>
  <section id="summary">
    <div class="summary">
      <div class="summary__radio">
        <button class="summary__radio-button" @click.prevent="tabActive = 1">
          Отправить CV
        </button>
        <button
          class="summary__radio-button summary__radio-button-green"
          @click.prevent="tabActive = 2"
        >
          Порекомендовать друга
        </button>
      </div>
      <div class="summary__me" :class="{ 'active-tab': tabActive === 1 }">
        <div class="summary__me-info">
          <div class="summary__title">
            <h2 class="title afterText summary__title-text">Отправить CV</h2>
            <img src="/points.svg" alt="point" class="summary__point" />
          </div>
          <p class="subtitle summary__subtitle">
            Не нашли подходящей вакансии? Не расстраивайтесь. Оставьте свое CV и
            наш HR свяжется с вами, если у нас откроется новая позиция
          </p>
          <div class="summary__forms">
            <input
              type="text"
              class="summary__form"
              placeholder="Имя и Фамилия"
            />
            <input type="text" class="summary__form" placeholder="Емейл" />
          </div>
          <div class="summary__load">
            <img
              src="/career/loadCV.png"
              alt="load"
              class="summary__load-image"
            />
            <p class="summary__load-title">Загрузить CV</p>
            <p class="summary__load-subtitle">Размер файла не более 2 Мб</p>
          </div>
          <textarea
            class="summary__textarea"
            placeholder="Ваш коментарий"
          ></textarea>
          <div class="summary__checkbox">
            <input type="checkbox" class="summary__checkbox-input" />
            <p class="summary__checkbox-text">
              Я согласен с Privacy policy MOJAM
            </p>
          </div>
          <button class="button__orange summary__button">Отправить CV</button>
        </div>
      </div>
      <div class="summary__friend" :class="{ 'active-tab': tabActive === 2 }">
        <div class="summary__friend-info">
          <div class="summary__title">
            <h2 class="title afterTextOrange">Порекомендовать друга</h2>
          </div>
          <p class="subtitle summary__subtitle-friend">
            У вас есть кого порекомендовать нам? Отправьте его контакт и в
            случае успешного трудоустройства вы получите вознаграждение
          </p>
          <div class="summary__forms">
            <input
              type="text"
              class="summary__form summary__form-black"
              placeholder="Ваше имя"
            />
            <input
              type="text"
              class="summary__form summary__form-black"
              placeholder="Ваш емейл"
            />
          </div>
          <div class="summary__forms summary__forms-friend">
            <input
              type="text"
              class="summary__form summary__form-black"
              placeholder="Имя и фамилия друга"
            />
            <input
              type="text"
              class="summary__form summary__form-black"
              placeholder="Контакт друга"
            />
          </div>
          <div class="summary__load">
            <img
              src="/career/loadCV.png"
              alt="load"
              class="summary__load-image"
            />
            <p class="summary__load-title">Загрузить CV друга</p>
            <p class="summary__load-subtitle summary__load-subtitle-friend">
              Размер файла не более 2 Мб
            </p>
          </div>
          <div class="summary__checkbox">
            <input
              type="checkbox"
              class="summary__checkbox-input summary__checkbox-input-friend"
            />
            <p class="summary__checkbox-text summary__checkbox-text-friend">
              Я согласен с Privacy policy MOJAM
            </p>
          </div>
          <button class="button__orange summary__button-friend">
            Отправить CV
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      tabActive: 1
    };
  }
};
</script>

<style lang="scss">
#summary {
  width: 100%;
  position: relative;
}

.summary {
  display: grid;
  grid-template-columns: 82.7rem 60.5rem;
  height: 72.6rem;

  &__me {
    background-color: $bgDark;

    &-info {
      width: 38rem;
      margin: auto;
      padding-left: 1.5rem;
      padding-top: 7rem;
    }
  }

  &__friend {
    background-color: $green;

    &-info {
      width: 38rem;
      margin: auto;
      padding-top: 7rem;
      padding-right: 2rem;
    }
  }

  &__title {
    display: flex;
    justify-content: space-between;
    align-items: flex-end;

    &-text {
      color: $white;
    }
  }

  &__subtitle {
    color: $white;
    padding-top: 4.7rem;
    width: 30rem;
    padding-left: 10rem;

    &-friend {
      color: $black;
      padding-top: 4.7rem;
      width: 29rem;
      padding-left: 10rem;
    }
  }

  &__point {
    position: absolute;
    left: 60.5rem;
    top: 5.5rem;
    width: 18rem;
  }

  &__forms {
    padding-top: 4.5rem;
    display: flex;
    align-items: center;
    justify-content: space-between;
    &-friend {
      padding-top: 2rem;
    }
  }

  &__form {
    width: 15rem;
    height: 3.5rem;
    padding: 0 1.5rem;
    border: 0.1rem solid $white;
    background: rgba(241, 241, 241, 0.05);
    font-family: GillLight;
    font-size: 1.2rem;
    color: $white;
    outline: none;
    &-black {
      border: 0.1rem solid $black;
      color: $black;
      background: rgba(14, 14, 14, 0.05);
      &::placeholder {
        color: rgba(14, 14, 14, 0.5);
      }
    }
  }

  &__load {
    display: flex;
    align-items: center;
    padding-top: 3rem;

    &-image {
      width: 2rem;
      padding-right: 1.1rem;
    }

    &-title {
      color: $orange;
      font-size: 1.6rem;
      font-weight: 500;
      padding-right: 1.5rem;
    }

    &-subtitle {
      color: $white;
      font-size: 1.2rem;
      letter-spacing: 0;
      &-friend {
        color: $black;
      }
    }
  }

  &__textarea {
    padding: 1.2rem;
    border: 0.1rem solid $white;
    background: rgba(241, 241, 241, 0.05);
    font-family: GillLight;
    font-size: 1.2rem;
    color: #f1f1f1;
    outline: none;
    width: 35.5rem;
    height: 6rem;
    margin-top: 3rem;
    resize: none;
  }

  &__checkbox {
    padding-top: 3rem;
    display: flex;
    align-items: center;

    &-input {
      width: 1.6rem;
      height: 1.6rem;
      margin: 0;
      appearance: none;
      background: none;
      border: 1px solid $white;
      &-friend {
        border: 1px solid $black;
      }
    }

    &-text {
      color: $white;
      font-size: 1.2rem;
      margin-left: 1.5rem;
      letter-spacing: 0;
      &-friend {
        color: $black;
      }
    }
  }

  &__button {
    margin-top: 6rem;
    &-friend {
      background: $black;
      color: $white;
      margin-top: 12rem;
    }
  }
}
.summary__radio {
  display: none;
}
@media screen and (max-width: 460px) {
  .summary {
    display: grid;
    grid-template-columns: 1fr;
    height: auto;

    &__radio {
      display: flex;
      width: 100%;
      height: auto;
      &-button {
        width: 50%;
        background: $bgDark;
        border: none;
        display: flex;
        box-sizing: border-box;
        font-size: 7.2rem;
        line-height: 8.2rem;
        padding: 14.4rem 8rem 8.8rem 8.8rem;
        color: $white;
        align-items: flex-end;
        text-align: left;
        position: relative;
        &::after {
          content: "";
          position: absolute;
          left: 8rem;
          bottom: 4.1rem;
          width: 40rem;
          height: 2px;
          background: $green;
        }
        &-green {
          background: $green;
          color: $black;
          &::after {
            background: $orange;
          }
        }
      }
    }
    &__me {
      padding-bottom: 15rem;
      display: none;
      &.active-tab {
        display: block;
      }

      &-info {
        width: 128.2rem;
        margin: 0 auto;
        padding: 0;
      }
    }

    &__friend {
      padding-bottom: 15rem;
      display: none;
      &.active-tab {
        display: block;
      }

      &-info {
        width: 128.2rem;
        margin: 0 auto;
        padding: 0;
      }
    }

    &__title {
      display: none;
      &-text {
        color: $white;
      }
    }

    &__subtitle {
      width: 112rem;
      font-size: 5.6rem;
      line-height: 6.4rem;
      padding: 13.2rem 0 22.8rem;

      &-friend {
        color: $black;
        width: 112rem;
        padding: 13.2rem 0 29.2rem;
        font-size: 5.6rem;
        line-height: 6.4rem;
      }
    }

    &__point {
      display: none;
    }

    &__forms {
      padding-top: 4.5rem;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding-bottom: 12rem;
      &-friend {
        padding-top: 2rem;
      }
    }

    &__form {
      width: 60rem;
      height: 14rem;
      padding: 0 6rem;
      border: 1px solid $white;
      font-size: 4.8rem;
      box-sizing: border-box;
      &-black {
        border: 1px solid $black;
        &::placeholder {
          color: rgba(14, 14, 14, 0.5);
        }
      }
    }

    &__load {
      display: flex;
      align-items: center;
      padding-top: 3rem;

      &-image {
        width: 8rem;
        padding-right: 4.4rem;
      }

      &-title {
        font-size: 6.4rem;
        padding-right: 6rem;
      }

      &-subtitle {
        font-size: 4.8rem;
        &-friend {
          color: $black;
        }
      }
    }

    &__textarea {
      padding: 4.8rem;
      border: 1px solid $white;
      font-size: 4.8rem;
      width: 100%;
      height: 36rem;
      margin-top: 12rem;
      box-sizing: border-box;
    }

    &__checkbox {
      padding-top: 12rem;

      &-input {
        width: 6.4rem;
        height: 6.4rem;
        margin: 0;
      }

      &-text {
        font-size: 4.8rem;
        margin-left: 6rem;
      }
    }

    &__button {
      margin: 0 auto;
      margin-top: 24rem;
      display: block;
      &-friend {
        background: $black;
        color: $white;
        margin: 0 auto;
        margin-top: 48rem;
        display: block;
      }
    }
  }
}
</style>
