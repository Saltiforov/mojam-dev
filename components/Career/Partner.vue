<template>
  <section id="partner">
    <div class="partner container">
      <h2 class="partner__title">Партнерская программа</h2>
      <p class="partner__subtitle">Если вы не нашли подходящу вакансию для себя - вы можете посоветовать нас cвоим
        друзьям. <br> <br> Мы считаем, что личне рекомендации эффективнее рекламы, поэтому поощряем пользователей,
        которые приводят нам
        новых сотрудников</p>
      <div class="partner__items flexBetween">
        <div class="partner__item">
          <h3 class="partner__item-count">01</h3>
          <h3 class="partner__item-title">Свяжитесь с нами</h3>
          <p class="partner__item-subtitle">Отправьте нам ссылку на LinkedIn кандидата и свои контактные данные
            воспользовавшись формой внизу страницы</p>
        </div>
        <div class="partner__item">
          <h3 class="partner__item-count">02</h3>
          <h3 class="partner__item-title">Прескрининг</h3>
          <p class="partner__item-subtitle">Если мы заинтересуемся кандидатом, мы направим вам сообщение об этом и будет
            уведомлять об изменении статуса кандидата</p>
        </div>
        <div class="partner__item">
          <h3 class="partner__item-count">03</h3>
          <h3 class="partner__item-title">Выплата вознаграждения</h3>
          <p class="partner__item-subtitle">В случае успешного трудоустройства кандидата вы получите существенное
            вознаграждение</p>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
#partner {
  width: 100%;
  height: 57rem;
  padding-top: 11.2rem;
}

.partner {
  &__title {
    font-size: 3rem;
    font-weight: 600;
    line-height: 3.6rem;
    letter-spacing: 0.12rem;
  }

  &__subtitle {
    width: 48.1rem;
    font-size: 1.6rem;
    line-height: 1.8rem;
    letter-spacing: 0;
    font-weight: 300;
    padding-top: 5rem;
    padding-left: 10rem;
  }

  &__items {
    padding-top: 5.6rem;
    width: 88rem;
    margin: auto;
  }

  &__item {
    width: 22rem;
    height: 19rem;
    background: #F5F8FC;
    border-radius: 1rem;
    padding: 2.3rem 3rem 6.6rem;

    &-count {
      font-size: 3rem;
      color: $green;
      line-height: 3.4rem;
    }

    &-title {
      font-size: 2rem;
      line-height: 2.3rem;
      letter-spacing: 0.03rem;
      padding-top: 2rem;
    }

    &-subtitle {
      letter-spacing: 0;
      font-size: 1.4rem;
      line-height: 1.6rem;
      padding-top: 5rem;
    }
  }
}

@media screen and (max-width: 460px) {
  #partner {
    padding-top: 21.6rem;
    height: 100%;
  }
  .partner {
    &__title {
      font-size: 9.6rem;
      line-height: 11.6rem;
      position: relative;
      padding-bottom: 18.8rem;

      &:after {
        content: '';
        position: absolute;
        top: 12.8rem;
        //width: 106rem;
        width: 99rem;
        left: 0;
        height: .8rem;
        background: $green;
      }
    }

    &__subtitle {
      font-size: 5.4rem;
      line-height: 6.4rem;
      width: 100%;
      padding: 0;
    }

    &__items {
      flex-direction: column;
      padding: 22.8rem 0 24rem;
    }

    &__item {
      width: 112rem;
      height: 112rem;
      margin-bottom: 8rem;
      padding: 9.2rem 12rem;
      box-sizing: border-box;

      &-count {
        font-size: 12rem;
        line-height: 13.6rem;

      }

      &-title {
        font-size: 8rem;
        line-height: 9.2rem;
        padding: 7.6rem 0 20.8rem;
      }

      &-subtitle {
        font-size: 5.4rem;
        line-height: 6.4rem;
      }
    }
  }
}
</style>
