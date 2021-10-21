<template>
  <main id="home">
    <FirstScreen
      :title="firstScreen.title"
      :subtitle="firstScreen.subtitle"
      :buttonOrange="firstScreen.buttonOrange"
      :buttonDark="firstScreen.buttonDark"
      :background="firstScreen.background"
      :bigScreen="true"
      :routeBtnOrange="firstScreen.routeBtnOrange"
    />
    <About />
    <Career />
    <Bonus :homePage="true"/>
    <Summary />
  </main>
</template>

<script>
import FirstScreen from '@/components/Home/FirstScreen'
import About from '@/components/Home/AboutUs'
import Career from '@/components/Home/Career'
import Bonus from '@/components/Home/Bonus'
import Summary from '@/components/Career/SendSummary'
export default {
  data() {
    return {
      firstScreen: {
        title: 'Мы строим игровые сервисы',
        subtitle: 'Которыми пользуются миллионы людей по всему миру',
        buttonOrange: 'Вакансии',
        buttonDark: 'Обратная связь',
        background: '/home/home-background.png',
        routeBtnOrange: '/career'
      }
    }
  },
  components: {
    FirstScreen,
    About,
    Career,
    Bonus,
    Summary
  }
}
</script>
<style lang="scss">
#home {

}
</style>
