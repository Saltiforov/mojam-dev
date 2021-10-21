<template>
  <section id="firstScreen" :style="`background-image: url('${background}');`">
    <div class="container">
      <div
        :class="
          bigScreen
            ? 'first-screen flexColumn'
            : 'first-screen-little first-screen flexColumn'
        "
      >
        <p v-if="crumbs" class="first-screen__crumbs">
          {{ crumbsActive }} <span>{{ crumbs }}</span>
        </p>
        <h1 class="first-screen__title">{{ title }}</h1>
        <p class="first-screen__subtitle">{{ subtitle }}</p>
        <div class="first-screen__buttons flexBetween">
          <nuxt-link :to="routeBtnOrange"
            ><button class="button__orange" v-if="buttonOrange">
              {{ buttonOrange }}
            </button></nuxt-link
          >
          <button class="button__dark" v-if="buttonDark">
            {{ buttonDark }}
          </button>
        </div>
      </div>
    </div>
    <img
      v-if="bigScreen"
      src="/mouse.svg"
      alt="mouse"
      class="first-screen__mouse flexCenter"
    />
  </section>
</template>
<script>
export default {
  props: [
    "title",
    "subtitle",
    "buttonOrange",
    "buttonDark",
    "background",
    "bigScreen",
    "crumbs",
    "crumbsActive",
    "routeBtnOrange"
  ]
};
</script>
<style lang="scss">
#firstScreen {
  background-repeat: no-repeat;
  background-size: 100%;
  width: 100%;
}
.first-screen {
  padding-top: 39.5rem;
  height: 20.4rem;
  &__title {
    font-size: 4rem;
    color: $white;
    line-height: 4.6rem;
  }
  &__subtitle {
    font-size: 2.4rem;
    line-height: 2.7rem;
    font-weight: 300;
    width: 44rem;
    color: $white;
    padding-bottom: 3.7rem;
    letter-spacing: 0;
  }
  &__buttons {
    width: 39.6rem;
  }
  &__mouse {
    width: 2rem;
    margin: auto;
    padding-top: 14rem;
    padding-bottom: 3rem;
  }
  &-little {
    padding-top: 27.5rem;
    padding-bottom: 12rem;
  }
  &__crumbs {
    position: absolute;
    color: $lightGrey;
    font-size: 1rem;
    line-height: 2rem;
    top: 11rem;
    span {
      color: $grey;
    }
  }
}
@media screen and (max-width: 460px) {
  #firstScreen {
    //background-size: 320%;
    background-size: 450%;
    background-position: -222rem 0rem;
  }
  .first-screen {
    padding-top: 106rem;
    height: auto;
    justify-content: flex-start;
    &__mouse {
      display: none;
    }
    &__title {
      font-size: 12rem;
      line-height: 13.8rem;
      margin-bottom: 8.2rem;
    }
    &__crumbs{
      display: none;
    }
    &__subtitle {
      font-size: 8rem;
      line-height: 9.1rem;
      width: 100%;
      padding-bottom: 22rem;
    }
    &__buttons {
      width: 67.6rem;
      height: 50.8rem;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      margin: 0 auto;
      padding-bottom: 24rem;
    }
  }
}
</style>
