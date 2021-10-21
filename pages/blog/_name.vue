<template>
  <main>
    <section id="blog">
      <div class="container">
        <div class="blog">
          <p class="blog__crumbs">
            {{ crumbsActive }} {{ crumbs }} <span>/ {{ title }}</span>
          </p>
          <blog-item :item="blog" />
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import BlogItem from "../../components/Blog/BlogItem";

export default {
  components: {
    BlogItem
  },
  data() {
    return {
      title: "7 сервисов для бизнес-аналитика в проектах Internet of Things",
      crumbsActive: "Главная /",
      crumbs: "Наша команда",
      blog: {
        title: "7 сервисов для бизнес-аналитика в проектах Internet of Things",
        blogDate: "13 мая 2021",
        aside:
          "В апреле 2021 года маркетинговое агентство IoT Analytics опубликовало статью The 7 Most Demanded IoT System Integration Services. Я предлагаю разобраться с тем, какие сервисы и почему являются критически важными для успеха IoT-проектов и в чем особенности бизнес-анализа для этого домена.",
        social: ["facebook.png", "linkedIn.png", "twitter.png"],
        desc: "Аутсорсинг-сервисы, наиболее востребованные в IoT",
        picturePath: "/blog/internetThings/internetThings-picture.png",
        picturePathAlt: "internetThings",
        news: {
          firstParagraph:
            "Обсуждение будет вращаться вокруг базовой диаграммы, которая рассматривает цепочку создания ценности как совокупность четырех этапов: стратегии, проектирования, реализации и эксплуатации. На каждом из этапов применимы те или иные сервисы, которые разделим на три категории, в зависимости от их востребованности: наиболее востребованные, часто запрашиваемые и редко запрашиваемые.",
          picturePath: "/blog/internetThings/descNews-picture.png",
          picturePathAlt: "descNews-picture",
          secondParagraph:
            "В апреле 2021 года маркетинговое агентство IoT Analytics опубликовало статью The 7 Most Demanded IoT System Integration Services. Я предлагаю разобраться с тем, какие сервисы и почему являются критически важными для успеха IoT-проектов и в чем особенности бизнес-анализа для этого домена.",
          thirdParagraph:
            "Статистика говорит о том, что 78% компаний, реализующих IoT-проекты, прибегают к помощи сторонних сервисов при интеграции. Почему сторонние сервисы здесь настолько востребованные? Одна из причин — то, что технологии IoT более сложные по сравнению с другими IT-технологиями. Кроме того, IoT требует владения навыками в смежных областях, которые находятся несколько в стороне от традиционного IT (например, встроенные системы и их информационная безопасность). Их, как правило, не изучают инженеры. К этому следует добавить навыки в облачных сервисах, больших данных и разработке приложений, в управлении подключением устройств.",
          fourthParagraph:
            "Ключевые ценности создаются на этапах проектирования и реализации. Как видим, наиболее важные для IoT-проектов семь сервисов."
        },
        lastNews: {
          title: "Последние новости",
          newsItems: [
            {
              blogActive: false,
              image: "/blog/blog1.png",
              info: "Почему пейнтбол укрепляет коллектив"
            },
            {
              blogActive: false,
              image: "/blog/blog2.png",
              info: "Пикник в стиле Geek как IT-шники отдыхали в Парке Горького"
            },
            {
              blogActive: true,
              image: "/blog/blog3.png",
              info:
                "Печенежское водохранилище вместо Мальдив. Отдыхаем во время локдауна"
            },
            {
              blogActive: false,
              image: "/blog/blog4.png",
              info: "Покупка NFT.Приобретаем право собственности на токен"
            }
          ]
        }
      }
    };
  }
};
</script>

<style lang="scss" scoped>
.blog {
  padding: 14.6rem 0 3.1rem 0;

  &__title {
    padding-top: 1rem;
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
  .blog {
    padding: 45.8rem 0 11.5rem 0;
    &__crumbs {
      display: none;
    }
  }
}
</style>
