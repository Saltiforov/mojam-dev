<template>
  <div class="blog__info">
    <div class="blog__info-column">
      <div class="blog__info-headline">
        <h1 class="blog__info-title">
          {{ item.title }}
        </h1>
        <p class="blog__info-subtitle">{{ item.blogDate }}</p>
      </div>
      <div class="blog__info-socials">
        <img
          v-for="social in item.social"
          :key="social.id"
          :src="`/social-networks/${social}`"
          :alt="social"
        />
      </div>
    </div>
    <div class="blog__info-picture">
      <img :src="`${item.picturePath}`" :alt="item.picturePathAlt" />
      <p class="blog__info-aside">
        {{ item.aside }}
      </p>
    </div>
    <div class="desc__info">
      <h2 class="desc__info-title">
        {{ item.desc }}
      </h2>
      <div class="desc__info-news desc__news">
        <p class="desc__news-text">
          {{ item.news.firstParagraph }}
        </p>
        <div class="desc__news-picture">
          <img
            :src="`${item.news.picturePath}`"
            :alt="item.news.picturePathAlt"
          />
        </div>
        <p class="desc__news-text">
          {{ item.news.secondParagraph }}
        </p>
        <p class="desc__news-text">
          {{ item.news.thirdParagraph }}
        </p>
        <p class="desc__news-text">
          {{ item.news.fourthParagraph }}
        </p>
      </div>
      <div class="last__news">
        <h2 class="last__news-title">
          {{ item.lastNews.title }}
        </h2>
        <div class="last__news-wrapper">
          <div
            class="last__news-item news__item"
            :class="{ 'news__item-active': news.blogActive }"
            v-for="news in item.lastNews.newsItems"
            :key="news.id"
          >
            <img :src="news.image" :alt="news.info" class="news__item-image" />
            <div class="news__item-text">
              <h2 class="news__item-name">{{ news.info }}</h2>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "BlogItem",
  props: {
    item: {
      type: Object,
      default: {
        title: {
          type: String,
          default: ""
        },
        blogDate: {
          type: String,
          default: ""
        },
        aside: {
          type: String,
          default: ""
        },
        social: {
          type: Array,
          default: []
        },
        desc: {
          type: String,
          default: ""
        },
        news: {
          type: Object,
          default: {}
        }
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.blog__info {
  &-column {
    display: flex;
    justify-content: space-between;
    margin-bottom: 0.75rem;
  }

  &-headline {
    width: 44.4rem;
    margin-left: 9.5rem;
  }

  &-title {
    font-size: 3rem;
    line-height: 3.4rem;
    position: relative;
  }

  &-subtitle {
    font-size: 1.2rem;
    line-height: 1.4rem;
    color: rgba(0, 0, 0, 0.5);
    padding-top: 0.5rem;
  }

  &-picture {
    display: flex;
    flex-direction: column;
  }

  &-socials {
    display: flex;
    align-items: flex-end;
    margin-bottom: 1.8rem;
    cursor: pointer;
    img {
      width: 2rem;
      height: 2rem;
    }
    img:nth-child(2) {
      margin: 0 1.6rem;
    }
  }

  &-aside {
    margin: 2.7rem 30.1rem 0;
    font-size: 1.6rem;
    line-height: 1.8rem;
    text-align: left;
  }
}

.desc__info {
  &-title {
    font-size: 1.8rem;
    margin: 3.7rem 0 3.7rem 20rem;
  }

  &-news {
    margin: 0 30rem;
  }
  &-picture {
    display: flex;
    justify-content: center;
  }
}

.desc__news {
  &-text,
  &-picture {
    font-size: 1.6rem;
    line-height: 1.8rem;
    margin-bottom: 2.6rem;
  }
  img {
    max-width: 58rem;
  }
}

.last__news {
  &-title {
    font-size: 3rem;
    line-height: 3.4rem;
    position: relative;
    margin-bottom: 5rem;
    margin-left: 9.8rem;

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

  &-wrapper {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    margin: 0 20rem;
    gap: 20px;
  }
}
.news__item {
  border-radius: 10px;
  flex-direction: column;
  display: flex;
  overflow: hidden;
  &-active &-text {
    background: #f3bd4d;
    transform: translateY(0);
  }
  &-active &-image {
    border-radius: initial;
  }
  &-image {
    width: 100%;
    height: 18rem;
    object-fit: cover;
    border-radius: 10px;
  }
  &-text {
    padding: 1.5rem 1.1rem 1.2rem;
  }
}
@media screen and (max-width: 460px) {
  .blog__info {
    &-column {
      flex-direction: column;
      margin-bottom: 8rem;
    }
    &-headline {
      width: 100%;
      margin-left: 0;
    }
    &-title {
      font-size: 6.9rem;
      width: 100%;
      line-height: 8.4rem;
      letter-spacing: 0rem;
      position: relative;
    }
    &-subtitle {
      font-size: 4.5rem;
      line-height: 1.4rem;
      color: rgba(0, 0, 0, 0.5);
      padding-top: 3rem;
      position: relative;
      top: 4rem;
    }
    &-socials {
      margin-left: auto;
      img {
        width: 8rem;
        height: 8rem;
      }
      img + img {
        margin-left: 5rem !important;
      }
    }
    &-picture {
      img {
        height: 70.4rem;
        border-radius: 10px;
        margin-bottom: 10.8rem;
      }
    }
    &-aside {
      width: 100%;
      margin: 0;
      text-align: start;
      font-size: 5.6rem;
      line-height: 6.4rem;
      margin-bottom: 16.4rem;
      letter-spacing: 0;
      font-weight: 300;
    }
  }
  .desc__info {
    &-title {
      margin: 0;
      font-size: 6.4rem;
      line-height: 7.4rem;
      margin-bottom: 16.4rem;
    }
    &-news {
      margin: 0;
    }
  }
  .desc__news {
    &-text {
      width: 100%;
      margin: 0;
      text-align: start;
      font-size: 5.6rem;
      line-height: 6.4rem;
      margin-bottom: 12rem;
      letter-spacing: 0;
      font-weight: 300;
    }
    &-picture {
      margin-bottom: 10.8rem;
      img {
        width: 100%;
        max-width: 100%;
        height: 70.4rem;
        border-radius: 10px;
      }
    }
  }
  .last__news {
    &-title {
      font-size: 9.6rem;
      line-height: 11.2rem;
      position: relative;
      margin-bottom: 20rem;
      margin-left: 0;
      &:after {
        content: "";
        position: absolute;
        top: 12rem;
        right: 0;
        left: 0;
        bottom: 0;
        width: 40rem;
        height: 1rem;
        background: #41b7a8;
      }
    }
    &-wrapper {
      grid-template-columns: repeat(1, 1fr);
      margin: 0;
      gap: 12rem;
    }
  }
  .news__item {
    margin: 0 auto;
    &-image {
      width: 72rem;
      height: 72rem;
    }
    &-text {
      padding: 5.5rem 1.1rem 4.2rem;
    }
    &-name {
      font-size: 6.4rem;
      line-height: 7.4rem;
      width: 60rem;
      margin: 0 auto;
    }
  }
}
</style>
