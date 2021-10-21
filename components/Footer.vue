<template>
  <footer>
    <div class="container footer">
      <div class="footer__logo flexColumn">
        <img src="/logo.svg" alt="logo" class="footer__logo-img">
        <p class="footer__logo-text">Copyright © 2015 - 2021.
          All Rights Reserved.</p>
      </div>
      <ul class="footer__column">
        <li class="footer__column-list">
          <a href="#" class="footer__column-link">Карьера в компании</a>
        </li>
        <li class="footer__column-list">
          <a href="#" class="footer__column-link">Бонусы сотрудникам</a>
        </li>
      </ul>
      <ul class="footer__column">
        <li class="footer__column-list">
          <a href="#" class="footer__column-link">Наша команда</a>
        </li>
        <li class="footer__column-list">
          <a href="#" class="footer__column-link">Истории</a>
        </li>
<!--        <li class="footer__column-list">-->
<!--          <a href="#" class="footer__column-link">О нас</a>-->
<!--        </li>-->
      </ul>
      <ul class="footer__column">
        <li class="footer__column-list">
          <a href="#" class="footer__column-link footer__link-grey">Контакты</a>
        </li>
        <li class="footer__column-list">
          <a href="#" class="footer__column-link footer__link-grey">Privacy policy</a>
        </li>
      </ul>
    </div>
  </footer>
</template>
<style lang="scss">
footer {
  width: 100%;
  height: 16.7rem;
  background-color: $black;
}

.footer {
  display: grid;
  grid-template-columns: 15rem 28rem 26rem 30.6rem;
  justify-items: flex-end;
  padding-top: 3.5rem;

  &__logo {
    text-align: center;
    height: 7.5rem;
    align-items: center;

    &-img {
      width: 8.43rem;
    }

    &-text {
      font-size: 1rem;
      font-weight: 300;
      line-height: 1.1rem;
      color: rgba(241, 241, 241, 0.5);
    }
  }

  &__column {
    &-list {
      padding-bottom: 1.7rem;
    }

    &-link {
      font-size: 1.4rem;
      color: $white;
      line-height: 1.7rem;
    }
  }

  &__link {
    &-grey {
      color: $grey;
      font-size: 1.6rem;
    }
  }
}

@media screen and (max-width: 460px) {
  footer {
    height: 116rem;
  }
  .footer {
    //grid-template-rows: 20.4rem 20.4rem 7.2rem;
    grid-template-rows: 1fr 0.5fr 0.5fr;
    grid-template-columns: 1fr 1fr;
    justify-items: center;
    grid-template-areas: "logo logo"
    "footer-column-1 footer-column-2"
    "privacy privacy";

    &__logo {
      grid-area: logo;
      padding-top: 14rem;
      height: 20.4rem;
      padding-bottom: 20.4rem;

      &-img {
        width: 33.6rem;
        height: 6.4rem;
      }

      &-text {
        font-size: 4rem;
        line-height: 4.4rem;
        width: 43rem;
      }
    }

    &__column {
      &:nth-child(3){
        margin-left: -8rem;
        //margin-left: -14rem;
        grid-area: footer-column-2;
      }
      &:nth-child(2){
        margin-left: -8rem;
        //margin-left: -14rem;
        grid-area: footer-column-1;
      }
      &:last-child {
        display: flex;
        grid-area: privacy;
        padding-top: 14.8rem;
        li:first-child {
          padding-right: 40rem;
        }
      }

      &-list {
          padding-bottom: 6.8rem;
      }

      &-link {
        font-size: 5.6rem;
        line-height: 6.4rem;
      }
    }

    &__link-grey {
      font-size: 6.4rem;
      line-height: 7.2rem;
    }

  }
}
</style>
