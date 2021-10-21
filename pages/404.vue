<template>
  <main>
    <section id="error-page">
      <h2 class="error-page__title">Ой, кажется тут никого нет!</h2>
      <p class="error-page__text">
        Вернитесь на <span class="error-page__text-orange">главную</span>!
      </p>
    </section>
  </main>
</template>

<script>
export default {};
</script>

<style lang="scss">
#error-page {
  background: no-repeat url("../static/404/404.png") center/cover;
  padding-top: 57.4rem;
  padding-bottom: 9.3rem;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.error-page {
  &__title {
    font-size: 2.4rem;
    line-height: 2.8rem;
    letter-spacing: 0;
    color: $white;
    margin-bottom: 2rem;
  }
  &__text {
    font-size: 1.6rem;
    line-height: 1.8rem;
    letter-spacing: 0;
    color: $white;
    &-orange {
      color: $orange;
    }
  }
}
@media (max-width: 460px) {
  #error-page {
    background: no-repeat url("../static/404/404.png") center/158%;
    padding-top: 100rem;
    padding-bottom: 18rem;
    background-position-y: 0rem;
  }
  .error-page {
    &__title {
      font-size: 8rem;
      line-height: 9rem;
      margin-bottom: 8rem;
    }
    &__text {
      font-size: 5.6rem;
      line-height: 6.4rem;
    }
  }
}
</style>
