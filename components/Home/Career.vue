<template>
  <section id="career">
    <div class="career container">
      <div class="career__image">
        <img
          src="/home/career/points-top-right.svg"
          alt="points"
          class="career__image-right"
        />
      </div>
      <h2 class="career__title">Карьера</h2>
      <div class="career__vacancies">
        <div class="career__vacancies-last">
          <h3 class="career__vacancies-last-title">
            Последние вакансии
          </h3>
          <div class="career__vacancies-last-items flexBetween">
            <div
              class="item__vacancy"
              v-for="item of items"
              :style="`border: .2rem solid ${item.border}`"
            >
              <h5
                class="item__vacancy-type"
                :style="`color: ${item.typeColor}`"
              >
                {{ item.type }}
              </h5>
              <h4 class="item__vacancy-title">{{ item.title }}</h4>
              <div class="flex">
                <img
                  :src="item.img"
                  :alt="item.type"
                  :style="
                    `width: ${width > 460 ? item.imgSize : item.imgSize * 4}rem`
                  "
                />
                <img
                  v-if="item.img2"
                  :src="item.img2"
                  :alt="item.type"
                  :style="
                    `width: ${
                      width > 460 ? item.imgSize2 : item.imgSize2 * 4
                    }rem`
                  "
                  class="item__vacancy-second-image"
                />
              </div>
            </div>
          </div>
        </div>
        <div class="career__vacancies-info">
          <p class="career__vacancies-info-text">
            Мы рады профессионалам, знающим толк в своем деле. Возможно это
            именно вы. Включайтесь в нашу команду
          </p>
          <button class="button__orange">Больше вакансий</button>
        </div>
      </div>
    </div>
    <img
      src="/home/career/points-bottom-left.svg"
      alt="points"
      class="career__point"
    />
    <img
      src="/home/career/Intersect.svg"
      alt="Intersect"
      class="career__intersect"
    />
  </section>
</template>
<script>
export default {
  data() {
    return {
      width: 0,
      items: [
        {
          type: "Development",
          typeColor: "#8F78E9",
          title: "Senior PHP developer",
          img: "/vacancy/php.svg",
          imgSize: 4,
          border: "#1D1D1D"
        },
        {
          type: "Marketing & Communication",
          typeColor: "#1D1D1D",
          title: "YouTube\\Twitch manager",
          img: "/vacancy/youtube.svg",
          img2: "/vacancy/twitch.svg",
          imgSize: 3,
          imgSize2: 2.2,
          border: "#F3BD4D"
        },
        {
          type: "Design",
          typeColor: "#789FE9",
          title: "Senior UI/UX designer",
          img: "/vacancy/UX.svg",
          imgSize: 7,
          border: "#1D1D1D"
        }
      ]
    };
  },
  methods: {
    updateWidth() {
      this.width = window.innerWidth;
    }
  },
  created() {
    window.addEventListener("resize", this.updateWidth);
    this.updateWidth();
  }
};
</script>
<style lang="scss">
#career {
  background-color: $bgDark;
  width: 100%;
  height: 45.5rem;
  position: relative;
}
.career {
  padding-top: 7.1rem;
  z-index: 1;
  position: relative;
  &__image {
    display: flex;
    justify-content: flex-end;
    width: 92.5%;
    &-right {
      width: 9.2rem;
    }
  }
  &__point {
    position: absolute;
    bottom: 3rem;
    z-index: 0;
    width: 17.4rem;
  }
  &__intersect {
    position: absolute;
    bottom: 0;
    right: 1rem;
    z-index: 0;
    width: 35.1rem;
  }
  &__title {
    font-size: 3rem;
    color: #f1f1f1;
    line-height: 3.4rem;
    border-bottom: 0.2rem solid #41b7a8;
    padding-bottom: 0.3rem;
    width: 11rem;
    margin: auto;
    position: relative;
    left: 6.2rem;
    top: 2.2rem;
  }
  &__vacancies {
    padding-top: 3.5rem;
    display: grid;
    grid-template-columns: 58rem 37rem;
    grid-gap: 12rem;
    &-last {
      &-title {
        font-size: 2rem;
        line-height: 2.3rem;
        color: $white;
        letter-spacing: 0.02rem;
      }
      &-items {
        padding-top: 2.5rem;
      }
    }
    &-info {
      &-text {
        color: #f1f1f1;
        font-size: 1.6rem;
        font-weight: 300;
        line-height: 1.8rem;
        padding-top: 4.5rem;
        letter-spacing: 0;
        padding-bottom: 5.56rem;
      }
    }
  }
}
@media screen and (max-width: 460px) {
  #career {
    height: auto;
    position: relative;
    .button__orange {
      display: none;
    }
  }
  .career {
    padding-top: 20.8rem;
    padding-bottom: 24rem;
    &__image {
      display: none;
    }
    &__point {
      display: none;
    }
    &__intersect {
      display: none;
    }
    &__title {
      font-size: 9.6rem;
      line-height: 11.2rem;
      position: relative;
      margin-bottom: 18rem;
      margin-left: 0;
      border: none;
      width: auto;
      top: 0;
      left: 0;
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
    &__vacancies {
      padding: 0;
      display: flex;
      flex-direction: column-reverse;
      &-last {
        &-title {
          font-size: 8rem;
          line-height: 9.2rem;
          margin-bottom: 22rem;
        }
        &-items {
          padding: 0;
          margin: auto;
          flex-direction: column;
        }
      }
      &-info {
        &-text {
          padding: 0;
          font-size: 5.6rem;
          line-height: 6.4rem;
          margin-bottom: 11.1rem;
        }
      }
    }
  }
}
</style>
