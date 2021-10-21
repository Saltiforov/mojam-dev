<template>
  <main>
    <FirstScreen
      :title="firstScreen.title"
      :subtitle="firstScreen.subtitle"
      :buttonOrange="firstScreen.buttonOrange"
      :buttonDark="firstScreen.buttonDark"
      :background="firstScreen.background"
      :crumbsActive="firstScreen.crumbActive"
      :crumbs="firstScreen.crumbs"
      :bigScreen="false"
      :routeBtnOrange="firstScreen.routeBtnOrange"
    />
    <Vacancy />
    <Bonus :homePage="false" />
    <Info />
    <Partner />
<!--    <Summary />-->
  </main>
</template>
<script>
import FirstScreen from '@/components/Home/FirstScreen'
import Vacancy from '@/components/Career/Vacancy'
import Bonus from '@/components/Home/Bonus'
import Info from '@/components/Career/Info'
import Partner from '@/components/Career/Partner'
import Summary from '@/components/Career/SendSummary'
export default {
  data() {
    return {
      firstScreen: {
        title: 'Мы нанимаем, потому что растем',
        subtitle: 'Приходите и вы наверняка останетесь надолго!',
        buttonOrange: 'Перейти к вакансиям',
        buttonDark: 'Показать нам свое CV',
        background: '/career/background.png',
        crumbActive: 'Главная /',
        crumbs: 'Карьера',
        routeBtnOrange: '/',
      }
    }
  },
  components: {
    FirstScreen,
    Vacancy,
    Bonus,
    Info,
    Partner,
    Summary,
  }
}
</script>
