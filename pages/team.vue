<template>
  <main>
    <section id="team">
      <div class="container">
        <div class="team flexColumn">
          <p class="team__crumbs">
            {{ crumbsActive }} <span>{{ crumbs }}</span>
          </p>
          <h1 class="team__title">
            {{ title }}
          </h1>
          <div class="container-s">
            <div class="flexColumn">
              <p class="team__subtitle">{{ subtitle }}</p>
              <div class="team__wrapper">
                <team-item
                  v-for="(item, index) in teams"
                  :key="index"
                  :item="item"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import TeamItem from "../components/team/TeamItem.vue";
export default {
  components: { TeamItem },
  data() {
    return {
      title: "Наша команда",
      subtitle: "Мы любим, то что делаем",
      crumbsActive: "Главная /",
      crumbs: "Наша команда",
      teams: [
        {
          teamActive: false,
          image: "/team/maria.png",
          position: "Middle UI/UX Designer",
          name: "Мария Потапова",
          info: "",
          color: "#789FE9"
        },
        {
          teamActive: false,
          image: "/team/stepan.png",
          position: "Ruby Software Engineer",
          name: "Степан Фролов",
          info: "",
          color: "#8F78E9"
        },
        {
          teamActive: true,
          image: "/team/andrey.png",
          position: "",
          name: "",
          info:
            "5 лет в компании. Любит кататься на велосипеде и футбол. Ведет блог на habr.com",
          color: ""
        },
        {
          teamActive: false,
          image: "/team/arina.png",
          position: "CTO",
          name: "Арина Карпова",
          info: "",
          color: "#24BCA1"
        },
        {
          teamActive: false,
          image: "/team/anna.png",
          position: "Front-End Engineer ",
          name: "Анна Фадеева",
          info: "",
          color: "#8F78E9"
        },
        {
          teamActive: false,
          image: "/team/artem.png",
          position: "Content Writer",
          name: "Артём Андреев",
          info: "",
          color: "#1D1D1D"
        }
      ]
    };
  }
};
</script>

<style lang="scss">
.team {
  padding: 14.6rem 0 11.5rem 0;

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
  &__title {
    font-size: 3rem;
    line-height: 3.4rem;
    position: relative;
    margin-left: 10rem;
    margin-bottom: 5rem;

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
  &__subtitle {
    font-size: 1.6rem;
    line-height: 1.82rem;
    position: relative;
    margin-bottom: 5.6rem;
    letter-spacing: 0;
  }
  &__wrapper {
    display: grid;
    grid-template-columns: repeat(3, 18.1rem);
    grid-template-rows: repeat(1, 32.8rem);
    gap: 3rem 11.9rem;
  }
}

@media screen and (max-width: 460px) {
  .team {
    padding: 45.8rem 0 11.5rem 0;
    &__crumbs {
      display: none;
    }
    &__container {
      width: 100%;
    }
    &__title {
      font-size: 9.6rem;
      line-height: 11.2rem;
      position: relative;
      margin-bottom: 21rem;
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
    &__subtitle {
      font-size: 6.4rem;
      margin-bottom: 13.5rem;
      margin-left: 0;
    }
    &__wrapper {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-rows: 1fr;
      gap: 12rem;
    }
  }
}
</style>
