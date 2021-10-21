<template>
  <main>
    <section id="blog">
      <div class="container">
        <div class="blog">
          <p class="blog__crumbs">
            {{ crumbsActive }} <span>{{ crumbs }}</span>
          </p>
          <nuxt-link to="blog/123">
            <blog-cart :item="blogs[0]" :first-item="true"></blog-cart>
          </nuxt-link>
          <div class="blog__wrapper">
            <nuxt-link
              to="blog/123"
              v-for="(item, index) in blogs.slice(1)"
              :key="index"
            >
              <blog-cart :item="item"></blog-cart>
            </nuxt-link>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import BlogCart from "../../components/Blog/BlogCart.vue";
export default {
  components: { BlogCart },
  data() {
    return {
      crumbsActive: "Главная /",
      crumbs: "Истории",
      blogs: [
        {
          active: false,
          image: "/blog/blog1.png",
          title: "Почему пейнтбол укрепляет коллектив",
          text:
            "Отдел QA одержал победу над разработчиками и показал кто главный"
        },
        {
          active: false,
          image: "/blog/blog2.png",
          title: "Пикник в стиле Geek: как IT-шники отдыхали в Парке Горького",
          text:
            "Весь день в основном зале инкубатора проходил питчинг стартапов. Молодые команды, разрабатывающие инновационные идеи, презентовали свои концепции..."
        },
        {
          active: false,
          image: "/blog/blog3.png",
          title:
            "Печенежское водохранилище вместо Мальдив. Отдыхаем во время локдауна ",
          text:
            'Здесь можно отдохнуть как дикарем, прихватив с собой палатку, мангал и другой инвентарь для пикника, так и "цивилизованно", сняв домик или беседку на побережье.'
        },
        {
          active: false,
          image: "/blog/blog4.png",
          title:
            "Покупка NFT. Приобретаем право собственности на токен или право интеллектуальной собственности?",
          text:
            "Начало 2021 года ознаменовалось новым витком в истории развития искусства – художник Майк Винкельманн, более известный как Бипл (Beeple)..."
        },
        {
          active: true,
          image: "/blog/blog5.png",
          title: "12 книг по управлению, машинному обучению и продуктивности",
          text:
            "Писать статью на тему «лучших книг» — это упражнение на минимализм, ведь нужно выбрать только то, что было и будет актуальным еще долгое время..."
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.blog {
  padding: 14.6rem 0 7.5rem 0;
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
  &__wrapper {
    display: grid;
    grid-template-columns: repeat(2, 58rem);
    grid-template-rows: repeat(1, 49.5rem);
    gap: 5.5rem 2rem;
  }
}

@media screen and (max-width: 460px) {
  .blog {
    padding: 45.8rem 0 11.5rem 0;
    &__crumbs {
      display: none;
    }
    &__wrapper {
      display: grid;
      grid-template-columns: repeat(1, 100%);
      grid-template-rows: repeat(1, 108rem);
      gap: 5rem;
      a {
        width: 100%;
        height: 100%;
      }
    }
  }
}
</style>
