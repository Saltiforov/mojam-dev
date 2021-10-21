<template>
  <header>
    <div class="container-xl">
      <div class="header">
        <img src="/logo.svg" alt="logo" class="header__logo" />
        <div
          class="header__burger"
          :class="{ active: isBurgerActive }"
          @click.prevent="isBurgerActive = !isBurgerActive"
        >
          <span></span>
        </div>
        <nav class="header__navigation" :class="{ active: isBurgerActive }">
          <ul class="header__bulleted flexBetween">
            <li class="header__list">
              <nuxt-link to="/career" class="header__link"
                >Карьера в компании
              </nuxt-link>
            </li>
            <li class="header__list">
              <nuxt-link to="/" class="header__link"
                >Бонусы сотрудникам
              </nuxt-link>
            </li>
            <li class="header__list">
              <nuxt-link to="/team" class="header__link"
                >Наша команда
              </nuxt-link>
            </li>
            <li class="header__list">
              <a href="#" class="header__link">Истории</a>
            </li>
          </ul>
        </nav>
        <p class="lang">RU</p>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  data: () => ({
    isBurgerActive: false
  })
};
</script>
<style lang="scss">
header {
  position: absolute;
  top: 3.2rem;
  width: 100%;
  z-index: 1;
  background: none;
}

.header {
  display: grid;
  grid-template-columns: 63.8rem 51.4rem 12rem;
  align-items: center;

  &__logo {
    width: 12.6rem;
  }

  &__link {
    font-size: 1.4rem;
    line-height: 1.67rem;
    font-weight: 500;
  }

  &__networks {
    padding-left: 6rem;

    &-img {
      width: 1rem;

      &:first-child {
        width: 2rem;
      }
    }
  }
}
.lang {
  font-size: 1.4rem;
  line-height: 2rem;
  padding-left: 8rem;
  color: $white;
}
.header__burger {
  display: none;
}
@media screen and (max-width: 460px) {
  .header {
    top: 0;
    padding-top: 9.6rem;
    grid-template-columns: 41.2rem 50.4rem 41.2rem;
    &__logo {
      width: 50.4rem;
    }
  }
  .lang {
    font-size: 9.6rem;
    line-height: 11.2rem;
    text-align: right;
  }
  .header__navigation {
    display: none;
  }
  .header__burger {
    display: block;
    position: relative;
    width: 12rem;
    height: 8.8rem;
    z-index: 3;
    grid-column-start: 1;
    grid-row-start: 1;
    span {
      position: absolute;
      background-color: #fff;
      left: 0;
      width: 100%;
      height: 1.6rem;
      top: 3.5rem;
      transition: all 0.3s ease 0s;
    }

    &:before,
    &:after {
      content: "";
      background-color: #fff;
      position: absolute;
      width: 100%;
      height: 1.6rem;
      left: 0;
      transition: all 0.3s ease 0s;
    }
    &:before {
      top: 0;
    }
    &:after {
      bottom: 0;
    }
    &.active {
      color: #0e0e0e;
      width: 9.6rem;
      height: 9.6rem;
      grid-column-start: 3;
      margin-left: auto;
      span {
        transform: scale(0);
      }

      &:before {
        background-color: #0e0e0e;
        transform: rotate(45deg);
        top: 4rem;
      }

      &:after {
        background-color: #0e0e0e;
        transform: rotate(-45deg);
        bottom: 4rem;
      }
      .header {
        justify-items: flex-end;
      }
    }
  }
  .header__navigation {
    display: block;
    position: fixed;
    top: -100%;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: auto;
    transition: all 0.3s ease 0s;
    .header__link {
      font-size: 7.2rem;
      line-height: 8.4rem;
      font-weight: 600;
      color: #0e0e0e;
    }
    &.active {
      top: 0;
      background-color: white;
      padding-top: 36.8rem;

      .flexBetween {
        flex-direction: column;
        width: 120rem;
        padding: 0 12rem;
        align-items: initial;
      }
      .header__list {
        padding-bottom: 11.6rem;
        padding-top: 12.4rem;
        border-bottom: 1px solid #f5f8fc;
        &:first-child {
          padding-top: 0;
        }
      }

      .nuxt-link-exact-active::after {
        height: 1.2rem;
        width: 120rem;
        top: 18.5rem;
      }
    }
  }
}
</style>
