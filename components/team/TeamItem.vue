<template>
  <div class="team__item" :class="{ 'team__item-active': item.teamActive }">
    <img :src="item.image" :alt="item.name" class="team__item-image" />
    <div class="team__item-text">
      <p class="team__item-position" :style="{ color: item.color }">
        {{ item.position }}
      </p>
      <h2 class="team__item-name">{{ item.name }}</h2>
      <div class="team__item-info">
        <p class="team__item-info-text">
          {{ item.info }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      default: {
        teamActive: {
          type: Boolean,
          default: false
        },
        image: {
          type: String,
          default: ""
        },
        position: {
          type: String,
          default: ""
        },
        name: {
          type: String,
          default: ""
        },
        info: {
          type: String,
          default: ""
        },
        color: {
          type: String,
          default: "#1D1D1D"
        }
      }
    }
  }
};
</script>

<style lang="scss">
.team__item {
  border-radius: 10px;
  flex-direction: column;
  display: flex;
  overflow: hidden;

  &-image {
    width: 100%;
    height: 23rem;
    object-fit: cover;
    border-radius: 10px;
  }
  &-text {
    width: 100%;
    height: 100%;
    position: relative;
    overflow: hidden;
    padding: 2.7rem 0 2.2rem 0;
    display: flex;
    flex-direction: column;
  }
  &-position {
    font-size: 1.2rem;
    line-height: 1.4rem;
    margin-bottom: 0.9rem;
    letter-spacing: 0;
  }
  &-name {
    font-size: 2rem;
    line-height: 2.3rem;
    color: #000000;
    letter-spacing: 0;
  }
  &-info {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    transform: translateY(-100%);
    transition: transform 0.5s ease;
    padding: 1.2rem 1.5rem 2.2rem 1.5rem;
    &-text {
      font-size: 1.4rem;
      line-height: 1.6rem;
      font-weight: 300;
      letter-spacing: 0;
    }
  }
  &-active > &-image {
    border-radius: 10px 10px 0 0;
  }
  &-active &-info {
    background: #f3bd4d;
    transform: translateY(0);
  }
}
@media screen and (max-width: 460px) {
  .team__item {
    margin: 0 auto;
    height: auto;
    &-image {
      width: 72rem;
      height: 72rem;
    }
    &-text {
      padding: 8rem 1.1rem 13rem;
    }
    &-position {
      font-size: 5.6rem;
      line-height: 6.6rem;
      width: 60rem;
      margin: 0 auto;
      margin-bottom: 5rem;
    }
    &-name {
      font-size: 6.4rem;
      line-height: 7.4rem;
      color: #000000;
      letter-spacing: 0;
      width: 60rem;
      margin: 0 auto;
    }
    &-info {
      &-text {
        font-size: 5rem;
        line-height: 6rem;
        width: 60rem;
        margin: 0 auto;
      }
    }
  }
}
</style>
