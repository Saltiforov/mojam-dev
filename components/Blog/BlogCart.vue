<template>
  <article
    class="blog-card"
    :class="{ active: item.active, 'first-blog-card': firstItem }"
  >
    <img class="blog-card__image" :src="item.image" :alt="item.title" />
    <div class="blog-card__info">
      <h2 class="blog-card__info-title">{{ item.title }}</h2>
      <p class="blog-card__info-text">{{ item.text }}</p>
    </div>
  </article>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: {
        active: {
          type: Boolean,
          default: false
        },
        image: {
          type: String,
          default: ""
        },
        title: {
          type: String,
          default: ""
        },
        text: {
          type: String,
          default: ""
        }
      }
    },
    firstItem: {
      type: Boolean,
      default: false
    }
  }
};
</script>

<style lang="scss">
.blog-card {
  display: flex;
  width: 100%;
  height: 100%;
  border-radius: 10px;
  flex-direction: column;
  align-items: flex-end;
  &.active {
    position: relative;
    top: 2.3rem;
    > .blog-card {
      &__image {
        border-radius: 10px 10px 0 0;
      }
      &__info {
        background: $orange;
      }
    }
  }
  &__image {
    width: 100%;
    height: 32rem;
    border-radius: 10px;
    object-fit: cover;
    margin-right: 0;
  }
  &__info {
    display: flex;
    flex-direction: column;
    padding-top: 3.2rem;
    padding-bottom: 2.6rem;
    width: 100%;
    border-radius: 0 0 10px 10px;
    align-items: end;
    &-title {
      font-size: 2rem;
      line-height: 2.3rem;
      margin-bottom: 2rem;
      color: #000000;
      width: 48.1rem;
      margin-left: 9.9rem;
    }
    &-text {
      font-size: 1.6rem;
      line-height: 1.8rem;
      font-weight: 300;
      width: 38.1rem;
      color: #000000;
      margin-left: 9.9rem;
    }
  }
}
.first-blog-card {
  &.blog-card {
    display: flex;
    width: 100%;
    height: 34rem;
    flex-direction: row;
    align-items: flex-start;
    margin-bottom: 5.8rem;
  }
  .blog-card__info {
    display: flex;
    flex-direction: column;
    padding-top: 5.3rem;
    &-title {
      font-size: 3rem;
      line-height: 3.5rem;
      margin-bottom: 2rem;
      color: #000000;
      width: 44.1rem;
      margin-left: 0;
    }
    &-text {
      font-size: 1.6rem;
      line-height: 1.8rem;
      font-weight: 300;
      width: 34.1rem;
      margin-left: 0;
    }
  }
  > .blog-card {
    &__image {
      width: 68rem;
      height: 100%;
      border-radius: 10px;
      object-fit: cover;
      margin-right: 5.7rem;
    }
  }
}
@media screen and (max-width: 460px) {
  .blog-card {
    display: flex;
    width: 100%;
    height: 100%;
    border-radius: 10px;
    flex-direction: column;
    align-items: flex-start;
    &.active {
      position: relative;
      top: 2.3rem;
      > .blog-card {
        &__image {
          border-radius: 10px 10px 0 0;
        }
        &__info {
          padding-top: 7.3rem;
          background: $orange;
          padding-bottom: 3rem;
        }
      }
      .blog-card__info-title {
        margin-left: 8rem !important;
      }
    }
    &__image {
      width: 100%;
      height: 70.7rem;
      border-radius: 10px;
      object-fit: cover;
      margin-right: 0;
    }
    &__info {
      display: flex;
      flex-direction: column;
      padding-top: 6.3rem;
      padding-bottom: 2.6rem;
      width: 100%;
      border-radius: 0 0 10px 10px;
      align-items: end;
      &-title {
        font-size: 7.3rem;
        line-height: 8.5rem;
        margin-bottom: 2rem;
        color: #000000;
        width: 100%;
        margin-left: 0;
      }
      &-text {
        display: none;
      }
    }
  }
  .first-blog-card {
    &.blog-card {
      display: flex;
      width: 100%;
      height: 90rem;
      flex-direction: column;
      align-items: flex-start;
      margin-bottom: 9.2rem;
    }
    .blog-card__info {
      display: flex;
      flex-direction: column;
      padding-top: 6.3rem;
      &-title {
        font-size: 7.3rem;
        line-height: 8.5rem;
        margin-bottom: 2rem;
        color: #000000;
        width: 100%;
        margin-left: 0;
      }
      &-text {
        display: none;
      }
    }
    > .blog-card {
      &__image {
        width: 100%;
        height: 71rem;
        border-radius: 10px;
        object-fit: cover;
        margin-right: 0;
      }
    }
  }
}
</style>
