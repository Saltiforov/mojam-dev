<template>
  <section id="open__vacancy">
    <div class="container open__vacancy">
      <img src="/career/vacancy/point.svg" alt="point" class="open__vacancy-image">
      <div class="open__vacancy-info">
        <div class="open__vacancy-info-text">
          <h2 class="open__vacancy-info-title">Открытые вакансии</h2>
          <p class="open__vacancy-info-subtitle">
            Главная ценность нашей компании - люди. Именно поэтому мы делаем все для того, <br> чтобы наши сотрудники
            были
            уверены, что работают в самой лучшей компании в <br> мире. <br>
          </p>
          <p class="open__vacancy-info-subtitle second-subtitle">
            Мы постоянно нанимаем разработчиков, QA-инженеров, дизайнеров, <br> DevOps-инженеров, проектных и
            продуктовых
            менеджеров.
          </p>

          <!--          <p class="open__vacancy-info-subtitle">-->
          <!--            Главная ценность нашей компании - люди. Именно поэтому мы делаем все для того, <br> чтобы наши сотрудники были-->
          <!--            уверены, что работают в самой лучшей компании в <br> мире. <br>-->
          <!--            <br>-->
          <!--            Мы постоянно нанимаем разработчиков, QA-инженеров, дизайнеров, <br> DevOps-инженеров, проектных и продуктовых-->
          <!--            менеджеров.</p>-->
        </div>
        <div class="open__vacancy-items flexBetween">
          <div class="item__vacancy open__vacancy-item" v-for="item of items"
               :style="`border: .2rem solid ${item.border}`">
            <h5 class="item__vacancy-type" :style="`color: ${item.typeColor}`">{{ item.type }}</h5>
            <h4 class="item__vacancy-title">{{ item.title }}</h4>
            <div class="flex">
              <img :src="item.img" :alt="item.type" :style="`width: ${item.imgSize}rem`">
              <img v-if="item.img2" :src="item.img2" :alt="item.type" :style="`width: ${item.imgSize2}rem`"
                   class="item__vacancy-second-image">
              <img src="static/arrow.png" alt="arrow">
            </div>
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
          type: 'Development',
          typeColor: '#8F78E9',
          title: 'Senior PHP developer',
          img: '/vacancy/php.svg',
          imgSize: 4,
          border: '#FFFEFE'
        },
        {
          type: 'Marketing & Communication',
          typeColor: '#1D1D1D',
          title: 'YouTube\\Twitch manager',
          img: '/vacancy/youtube.svg',
          img2: '/vacancy/twitch.svg',
          imgSize: 3,
          imgSize2: 2.2,
          border: '#F3BD4D'
        },
        {
          type: 'Design',
          typeColor: '#789FE9',
          title: 'Senior UI/UX designer',
          img: '/vacancy/UX.svg',
          imgSize: 7,
          border: '#FFFEFE'
        },
        // {
        //   type: 'Marketing & Communication',
        //   typeColor: '#1D1D1D',
        //   title: 'Support Manager',
        //   img: '/vacancy/support.svg',
        //   imgSize: 2.4,
        //   border: '#FFFEFE'
        // },
        // {
        //   type: 'Design',
        //   typeColor: '#789FE9',
        //   title: 'Graphic Designer',
        //   img: '/vacancy/design.svg',
        //   imgSize: 2.4,
        //   border: '#FFFEFE'
        // },
        // {
        //   type: 'Management',
        //   typeColor: '#24BCA1',
        //   title: 'Senior Project manager',
        //   img: '/vacancy/youtube.svg',
        //   img2: '/vacancy/twitch.svg',
        //   imgSize2: 2.2,
        //   imgSize: 3,
        //   border: '#FFFEFE'
        // },
        // {
        //   type: 'Design',
        //   typeColor: '#789FE9',
        //   title: '3D Artist',
        //   img: '/vacancy/3D.svg',
        //   imgSize: 2.9,
        //   border: '#FFFEFE'
        // },
        // {
        //   type: 'Development',
        //   typeColor: '#8F78E9',
        //   title: 'Lead React Developer',
        //   img: '/vacancy/react.svg',
        //   imgSize: 2.2,
        //   border: '#FFFEFE'
        // },
      ]
    }
  }
}
</script>
<style lang="scss">
#open__vacancy {
  width: 100%;
  height: 71.5rem;
  position: relative;
  padding-top: 8.7rem;
}

.open__vacancy {
  display: grid;
  grid-template-columns: 20rem 78rem;

  &-image {
    width: 12.9rem;
  }

  &-info {
    padding-top: 2.6rem;

    &-title {
      font-size: 3rem;
      line-height: 3.4rem;
      position: relative;

      &::after {
        content: '';
        position: absolute;
        top: 3.8rem;
        left: 0;
        right: 0;
        bottom: 0;
        width: 10rem;
        height: .2rem;
        background: $green;
      }
    }

    &-subtitle {
      font-size: 1.6rem;
      line-height: 1.8rem;
      padding-top: 5rem;
      padding-left: 10rem;
      letter-spacing: 0;
    }

    .second-subtitle {
      padding-top: 2.5rem;
    }
  }

  &-items {
    padding-top: 5.4rem;
    flex-wrap: wrap;
  }

  &-item {
    margin-bottom: 1.6rem;
  }
}

@media screen and (max-width: 460px) {
  #open__vacancy {
    height: 100%;
  }
  .open__vacancy {
    grid-template-columns: 128rem;

    &-image {
      display: none;
    }

    &-info {
      &-title {
        font-size: 9.6rem;
        line-height: 11.2rem;

        &:after {
          width: 40rem;
          height: 0.8rem;
          top: 12.8rem;
        }
      }

      &-subtitle {
        padding-top: 11.2rem;
        font-size: 5.6rem;
        line-height: 6.4rem;
        font-weight: 300;

        br {
          display: none;
        }
      }

      .second-subtitle {
        padding-top: 10rem;
      }
    }

    &-items {
      flex-direction: column;
      justify-content: initial;
      align-items: center;
      padding: 25.2rem 0 25.2rem;

      .item__vacancy {
        &:nth-child(2) {
          position: relative;

          &:after,
          &:before {
            content: '';
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
      }
    }
    .flex {
      img {
        width: 16rem !important;
        height: 8rem;
      }
    }
  }
  .open__vacancy-image {
    display: none;
  }
  .item__vacancy {
    box-sizing: border-box;
  }

}
</style>
