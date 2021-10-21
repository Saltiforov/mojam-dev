<template>
  <section id="about">
    <div class="about container">
      <img
        src="/home/about/point-about.svg"
        alt="point"
        class="about__point-left"
      />
      <div class="about__grid">
        <div class="about__images">
          <img src="/home/about/image-little.png" alt="image" />
          <img src="/home/about/image-big.png" alt="image" />
          <img src="/home/about/image-little-2.png" alt="image" />
        </div>
        <div class="about__info">
          <h2 class="about__info-title">О нас &nbsp;</h2>
          <div class="about__info-column">
            <p class="about__info-subtitle">
              Мы - продуктовая компания, которая разрабатывает сервисы CS:GO для
              геймеров. Каждый день ими пользуются десятки тысяч пользователей
              со всего мира. Наши продукты входят в топ крупнейших и наиболее
              успешных проектов в своем сегменте на мировом рынке. <br />
              <br />

              Став частью MOJAM вы сможете работать с быстро растущими и
              популярными продуктами среди многочисленной аудитории геймеров.
            </p>
            <img
              src="/home/about/point-about-right.svg"
              alt="point"
              class="about__info-point-right"
            />
          </div>
        </div>
      </div>
      <div class="about__numbers">
        <h2 class="about__numbers-title">MOJAM в цифрах</h2>
        <div class="about__numbers-items flexBetween">
          <div
            class="item about__numbers-item flexCenter"
            v-for="item of items"
          >
            <h3 class="about__numbers-item-title">{{ item.title }}</h3>
            <p class="about__numbers-item-subtitle">{{ item.subtitle }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          title: 61,
          subtitle: "человек в компании"
        },
        {
          title: "2.3 млн",
          subtitle: "активных юзеров"
        },
        {
          title: "x2",
          subtitle: "растем в два раза в год"
        },
        {
          title: 4,
          subtitle: "цифры в ряд смотрятся круче"
        }
      ]
    };
  }
};
</script>
<style lang="scss">
#about {
  height: 93rem;
  width: 100%;
}

.about {
  padding-top: 6rem;

  &__grid {
    display: grid;
    grid-template-columns: 50rem 68rem;
  }

  &__point {
    &-left {
      position: absolute;
      left: 8rem;
      z-index: 0;
      width: 12.9rem;
    }
  }

  &__images {
    padding-top: 6rem;
    position: relative;

    img {
      &:nth-child(1) {
        position: absolute;
        top: 27rem;
        left: 21.4rem;
        width: 15rem;
      }

      &:nth-child(2) {
        width: 28.5rem;
      }

      &:nth-child(3) {
        position: absolute;
        top: 1rem;
        left: 24rem;
        width: 10rem;
      }
    }
  }

  &__info {
    padding-top: 5.4rem;
    display: grid;
    grid-template-columns: 10.2rem 58rem;

    &-title {
      font-size: 3rem;
      line-height: 3.4rem;
      border-bottom: 0.2rem solid $green;
      padding-bottom: 0.3rem;
      align-self: self-start;
    }

    &-column {
      position: relative;
    }

    &-subtitle {
      font-size: 1.6rem;
      width: 57.7rem;
      padding-top: 8.5rem;
      letter-spacing: 0;
    }

    &-point {
      &-right {
        position: absolute;
        right: 0.5rem;
        z-index: 0;
        top: 37rem;
        width: 20.2rem;
      }
    }
  }

  &__numbers {
    padding-top: 19.3rem;

    &-title {
      font-size: 3rem;
      line-height: 3.4rem;
      position: relative;

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

    &-items {
      padding-top: 5.2rem;
      width: 78.1rem;
      margin: auto;
    }

    &-item {
      background: #f5f8fc;
      flex-direction: column;

      &-title {
        font-family: GillMedium, sans-serif;
        color: $green;
        font-size: 4rem;
        font-weight: 600;
        line-height: 4.8rem;
        text-align: center;
        padding-bottom: 1rem;
      }

      &-subtitle {
        font-size: 1.6rem;
        font-weight: 300;
        line-height: 1.8rem;
        text-align: center;
        letter-spacing: 0;
      }
    }
  }
}
@media screen and (max-width: 460px) {
  #about {
    height: auto;
  }
  .about {
    &__grid {
      grid-template-columns: 1fr;
    }
    &__images {
      display: none;
    }
    &__info {
      display: flex;
      flex-direction: column;
      &-title {
        font-size: 9.6rem;
        line-height: 11.2rem;
        position: relative;
        margin-bottom: 11.2rem;
        margin-left: 0;
        border: none;
        &:after {
          content: "";
          position: absolute;
          top: 12rem;
          right: 0;
          left: 0;
          bottom: 0;
          width: 40rem;
          height: 0.5rem;
          background: #41b7a8;
        }
      }
      &-subtitle {
        font-size: 5.6rem;
        line-height: 6.4rem;
        margin: 0;
        width: 100%;
      }
      &-point-right {
        display: none;
      }
    }
    &__numbers {
      padding-top: 20.8rem;
      &-title {
        font-size: 9.6rem;
        line-height: 11.2rem;
        position: relative;
        margin-bottom: 19.5rem;
        margin-left: 0;
        &:after {
          content: "";
          position: absolute;
          top: 12rem;
          right: 0;
          left: 0;
          bottom: 0;
          width: 40rem;
          height: 0.5rem;
          background: #41b7a8;
        }
      }
      &-items {
        flex-direction: column;
        width: 72rem;
        padding: 0;
      }
      &-item {
        width: 72rem;
        height: 72rem;
        & + & {
          margin-top: 8rem;
        }
        &-title {
          font-size: 16rem;
          line-height: 19rem;
        }
        &-subtitle {
          font-size: 6.4rem;
          line-height: 7.4rem;
        }
        &:nth-child(1) > &-subtitle,
        &:nth-child(4) > &-subtitle {
          width: 44rem;
        }
      }
    }
  }
}
</style>
